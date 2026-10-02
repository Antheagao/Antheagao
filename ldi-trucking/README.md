# LDI Trucking outreach

Outreach for LDI Trucking Inc.'s **AI & Automation Specialist** opening (Pomona, CA, $30–40/hr). The Indeed listing is paused, so this goes to them directly.

## Files

| File | What it is |
| --- | --- |
| `email-draft.md` | Email proposing remote work with a 30-minute weekly meeting, plus the 2 project examples the posting asks for |
| `LDI-Trucking-website-and-automation-concept.pdf` | 6-page PDF to attach: website concept with automation notes, then a roadmap appendix |
| `site-concept/index.html` | Source for the PDF. Open in a browser; the button in the purple bar shows or hides the automation notes |

## Who to contact

| | |
| --- | --- |
| Company | LDI Trucking Inc. · USDOT 1074419 · MC-446897 |
| Email | **ines@lditrucking.com** (Ines Guzman, Director of Safety; the email on LDI's FMCSA registration) |
| Phone | (909) 620-7001 · Fax (909) 620-8001 |
| HQ | 200 Erie St, Pomona, CA 91768 |
| Terminal | 2739 W McDowell Rd, Phoenix, AZ 85009 |
| President | Alexsander Kolesnikov (no public email found) |
| Website | lditrucking.com |

Calling the main line to ask who owns the hire and get their direct email is worth doing before or alongside the email.

## What the concept is based on

The current lditrucking.com site couldn't be loaded from the environment this was built in, so the concept uses public data instead: FMCSA records (about 140 tractors and 134 drivers, Satisfactory rating, hazmat certified, active interstate authority since 2008), a public LDI local-driver listing (home daily, 5 on/2 off, $800–1,300/week, $3,000 sign-on bonus) and the job posting itself. The page flags these figures for LDI to confirm.

Sources: [Rose Rocket](https://www.roserocket.com/trucking-company/ldi-trucking-inc-usdot-1074419), [CarrierSource](https://www.carriersource.io/carriers/ldi-trucking-inc), [Bubba.ai](https://bubba.ai/trucking-companies/california/pomona/ldi-trucking-inc-1074419), [Lanefinder](https://www.lanefinder.com/c/ldi_trucking_inc/1074419), [FMCSA SMS](https://ai.fmcsa.dot.gov/SMS/Carrier/1074419/CompleteProfile.aspx), [D&B](https://www.dnb.com/business-directory/company-profiles.ldi_trucking_inc.0b753b14c6d6207d71712d080dcc644c.html).

## Rebuilding the PDF

```bash
node -e "
const { chromium } = require('playwright');
(async () => {
  const b = await chromium.launch(); const p = await b.newPage();
  await p.goto('file://' + process.cwd() + '/site-concept/index.html');
  await p.emulateMedia({ media: 'print' });
  await p.pdf({ path: 'LDI-Trucking-website-and-automation-concept.pdf', format: 'Letter', printBackground: true, scale: 0.62,
    margin: { top: '0.3in', bottom: '0.3in', left: '0.3in', right: '0.3in' } });
  await b.close();
})();"
```
