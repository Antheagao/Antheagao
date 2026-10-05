# Hi, I'm Anthony Mendez

Systems software in C and C++: operating system kernels, compilers, and bare-metal firmware on RISC-V and Arm.

**Portfolio:** [anthonymendezswe.com](https://www.anthonymendezswe.com)

## Systems projects

- **[xv6-riscv](https://github.com/Antheagao/xv6-riscv)**: RISC-V kernel work in C on MIT's xv6.
  - Adds **lottery and stride schedulers**, 7 system calls, and **kernel threads** (`clone`/`join`). Threads share physical frames through private page tables.
  - A QEMU test harness checks each scheduler's fairness in CI, and it caught a real accounting bug in the round-robin path.
- **[compiler-analysis-pass](https://github.com/Antheagao/compiler-analysis-pass)**: an **LLVM liveness analysis pass** in C++17.
  - An iterative dataflow solver over the control-flow graph computes UEVAR, VARKILL, LIVEIN and LIVEOUT for each basic block.
  - CI checks the results against golden outputs.
- **[aarch64-firmware](https://github.com/Antheagao/aarch64-firmware)**: **bare-metal AArch64 firmware** written from the reset vector up. *In progress.*
  - Boots at EL3 on QEMU, the way real boot firmware does.
  - The [roadmap](https://github.com/Antheagao/aarch64-firmware/blob/main/docs/ROADMAP.md) builds toward EL1 hand-off, the MMU, GICv3, PSCI multi-core bring-up, and Armv9 feature enablement (SVE2, PAC/BTI, MTE).

**Toolbox:** C · C++ · Python · GCC / Clang / LLVM · QEMU · GDB · Make / CMake · Linux · GitHub Actions

Every systems project builds and runs its tests in CI on every push. See the badge in each README.

## Also built

Backend and full-stack work in Java, Python and TypeScript:

- **[ecommerce-api](https://github.com/Antheagao/ecommerce-api)**: a Spring Boot commerce API. It has Stripe Checkout, signed idempotent webhooks, an order state machine, and admin refunds reconciled with Stripe. 260 tests (Testcontainers), Dockerized, with CI.
- **[doc-pilot](https://github.com/Antheagao/doc-pilot)**: AI document intelligence. A vision-language model extracts structured JSON with a confidence score per field, and low-confidence fields go to a human review queue. Evals and per-document cost tracking are built in.
- **[character-rater](https://github.com/Antheagao/character-rater)**: a Next.js + Fastify + Prisma app with an ETL pipeline from the Jikan API, auth and migrations.
