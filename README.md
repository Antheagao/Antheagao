# Hi, I'm Anthony Mendez

I build AI products and the backends behind them, with a systems background in C and C++ underneath.
I like owning the hard parts myself: retrieval, evals, observability, payments, and the occasional kernel.

**Portfolio:** [anthonymendezswe.com](https://www.anthonymendezswe.com)

## AI engineering

- **[doc-pilot](https://github.com/Antheagao/doc-pilot)**: AI document intelligence in FastAPI + Next.js.
  - A vision-language model extracts receipts, invoices and forms into structured JSON with a **confidence score per field**.
  - Low-confidence fields go to a **human review queue**, and every document records its model, prompt version, latency, tokens and cost.
  - Postgres `SKIP LOCKED` job queue, 212 tests across three CI jobs, plus a cost-capped live smoke suite against the real API.
- **[helpdeck](https://github.com/Antheagao/helpdeck)**: an embeddable AI support chatbot, one script tag on any page.
  - Implements the RAG pieces itself instead of pulling in a framework: **BM25 retrieval** over markdown docs, **token-budgeted memory** with rolling summarization, and streamed answers with citations.
  - An offline mock model keeps the whole product runnable and tested with zero API keys.
- **[spanlight](https://github.com/Antheagao/spanlight)**: self-hosted **LLM observability**, a local alternative to Langfuse or LangSmith.
  - Traces, spans, token and cost accounting, and p50/p95 latency per model, with a dashboard and span waterfall.
  - The Python SDK is stdlib-only and never takes the host app down if the collector is unreachable.

## Backend

- **[ecommerce-api](https://github.com/Antheagao/ecommerce-api)**: a payments-grade Spring Boot commerce API.
  - Stripe Checkout, signed idempotent webhooks, an order state machine, and admin refunds reconciled with Stripe.
  - 260 tests with Testcontainers, Dockerized, with CI.
- **[character-rater](https://github.com/Antheagao/character-rater)**: a Next.js + Fastify + Prisma app with an ETL pipeline from the Jikan API, auth and migrations.

## Systems

- **[xv6-riscv](https://github.com/Antheagao/xv6-riscv)**: RISC-V kernel work in C on MIT's xv6.
  - Adds **lottery and stride schedulers**, 7 system calls, and **kernel threads** (`clone`/`join`).
  - A QEMU test harness checks scheduler fairness in CI, and it caught a real accounting bug in the round-robin path.
- **[compiler-analysis-pass](https://github.com/Antheagao/compiler-analysis-pass)**: an **LLVM liveness analysis pass** in C++17, an iterative dataflow solver over the CFG checked against golden outputs in CI.
- **[aarch64-firmware](https://github.com/Antheagao/aarch64-firmware)**: **bare-metal AArch64 firmware** from the reset vector up, booting at EL3 on QEMU. *In progress.*

## Toolbox

- **Languages:** Python · TypeScript · Java · C · C++
- **AI:** Anthropic and OpenAI APIs · RAG · structured outputs · evals · LLM tracing
- **Backend:** FastAPI · Spring Boot · Express / Fastify · Next.js · PostgreSQL · Docker
- **Systems:** LLVM / Clang · QEMU · GDB · Linux · Make / CMake
- **Shipping:** GitHub Actions - every project above runs its tests in CI on every push
