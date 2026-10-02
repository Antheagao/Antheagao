# Email draft: LDI Trucking, AI & Automation Specialist

**To:** ines@lditrucking.com
**Subject:** AI & Automation Specialist: a remote proposal + automation ideas for LDI
**Attach:** your résumé (PDF) and `LDI-Trucking-website-and-automation-concept.pdf`

Before sending: fill in your phone number, and attach both files.

---

Hi Ines,

I saw LDI's AI & Automation Specialist posting on Indeed, but the listing has been paused, so I'm reaching out directly. I found your address on LDI's public carrier listing. If someone else is handling this hire, I'd appreciate it if you could forward this to them.

I'm a backend and AI engineer (Python, Java, TypeScript, SQL). I build working systems, not just prompts. Here are the examples the posting asked for:

**1. doc-pilot: AI document extraction with human review**
- **Problem:** turning messy scanned documents (receipts, invoices, forms) into clean data without retyping it, and without blindly trusting the AI.
- **Tools:** Python (FastAPI), Claude vision model, PostgreSQL, Next.js, Docker.
- **What I built:** the whole pipeline: upload, AI extraction with a confidence score on every field, a review queue that sends only the low-confidence fields to a person, and per-document cost tracking.
- **Result:** 99.4% field-level accuracy on a 25-document labeled test set at about a penny per document, and the review queue flagged every error the model made. I'd use the same pattern for BOLs, PODs, rate confirmations and medical cards.
- github.com/Antheagao/doc-pilot

**2. ecommerce-api: a payment integration that stays in sync**
- **Problem:** keeping orders and payments consistent between my system and Stripe, even when webhook events arrive twice or out of order.
- **Tools:** Java/Spring Boot, PostgreSQL, Stripe API, Docker, GitHub Actions CI.
- **What I built:** verified, idempotent webhook handling, an order state machine and admin refunds reconciled with Stripe, covered by 260 automated tests.
- **Result:** a duplicate or replayed payment event can't process an order twice. Connecting a TMS to accounting needs the same reliability.
- github.com/Antheagao/ecommerce-api

I also put together a concept for LDI (PDF attached): a refreshed website with a shipper quote form, driver quick-apply, self-serve POD lookup and a driver document hub, with notes on the automation behind each feature and a 90-day roadmap. Three ideas from it:

- **Expiration tracker:** CDLs, medical cards, MVRs, registrations, IFTA/IRP and insurance in one list, with automatic reminders at 60, 30 and 7 days. Typically a 1–2 week build, and a quick win for Safety.
- **BOL/POD to invoice packet:** a driver snaps a photo, AI reads the load number, signature and exceptions, and files it with the invoice.
- **Applicant speed-to-lead:** an instant text reply and automatic follow-ups so driver applicants don't go cold.

**My proposal:** I know the role is listed as in person. I'd like to propose doing it remotely, with:

- A short weekly meeting (30 minutes on Teams or Zoom) to demo what shipped and agree on the next priority
- On-site time when it matters: discovery days at the start to shadow each department, and training when something goes live
- Everything documented and monitored, with driver and employee data kept in LDI-controlled accounts

To keep it low-risk for LDI, I'm happy to start with the practical exercise mentioned in the posting, or a short pilot on one workflow (the expiration tracker is a good candidate), so you can judge the work before committing to anything longer.

Would you have 20 minutes next week for a call? My résumé is attached.

Thank you,
Anthony Mendez
[Your phone number]
anthonymendezswe.com
github.com/Antheagao
