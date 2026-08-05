# Isaiah A. Faluyi

**AI Engineer — production LLM systems, RAG, and the infrastructure that keeps them reliable.**

Most LLM projects demo beautifully and fall apart in production. I work on the ones that can't.

I build retrieval and agent-instruction infrastructure for multi-tenant agentic platforms, extraction pipelines that turn unstructured real-world inputs — scans, handwriting, faxes, forms — into structured, trustworthy data, and the evaluation infrastructure that proves the accuracy number is real rather than the best of five runs.

Currently: the AI layer of a multi-tenant agentic platform — dual RAG over Pinecone and ChromaDB, guardrailed instruction capture, and namespace-scoped context for autonomous agents. Most recently: production healthcare intake automation, where a single misread character in a medical code is a total failure.

---

### What I work on

**Retrieval & agent memory** — RAG over vector databases, embeddings, semantic search, namespace-scoped context, guardrailed instruction capture

**LLM infrastructure** — prompt versioning and composition, multi-tenant resolvers, RBAC and tenant isolation

**Document AI & extraction** — OCR, handwriting, LLM extraction, layered validation and correction pipelines

**Evaluation & reliability** — golden regression suites, non-determinism handling, confidence gating, hallucination containment, tracing and alerting

**Agentic systems** — multi-agent orchestration, tool use, LLM-driven workflows

**Backend** — Python, Java, FastAPI, Django, AWS, distributed services

---

### How I think about LLM systems

A few things I've learned building AI into domains where being wrong has consequences:

- **A correction should never be a guess.** Every automated fix in a pipeline I build requires independent evidence — a clean copy elsewhere in the document, an explicit label, a second source agreeing at the same coordinate. Bounded, gated, unique-nearest. Otherwise you are not correcting errors, you are manufacturing confident ones.

- **Report the distribution, not the best run.** Vision models read handwriting differently every time. If your accuracy swings 88–92% run to run, the honest number is "high-80s to low-90s," not the 92 you screenshot. A single run's score is a draw from a distribution.

- **Retrieval is a permissions problem before it's a relevance problem.** In a multi-tenant system, "what should the model see" and "what is this tenant entitled to see" are the same question. Namespace scoping isn't an optimization you add later; it's the boundary the whole retrieval layer is built around.

- **Anything a user can teach an agent, they can teach it wrong.** Letting people write natural-language instructions that agents later obey is a fast way to ship a system that misbehaves confidently. Instructions get validated against guardrails before they persist — the gate belongs on the write path, not the read path.

- **Classify failures by lever, not by symptom.** Some misses are pipeline bugs. Some are perception floors that no amount of engineering will fix. Knowing which is which is the difference between a productive quarter and a wasted one.

- **Codes are the worst possible OCR target.** No language priors, no redundancy, exact-match scoring, character-level precision. A `3` scrawled like a `5` is an unrecoverable coin flip. The leverage is structural — find the clean copy printed elsewhere — not in expecting perception to nail every glyph.

---

### Stack

`Python` `Java` `FastAPI` `SQLAlchemy` `Django` `Flask` `OpenAI` `Anthropic`
`Pinecone` `ChromaDB` `AWS (Lambda, S3, API Gateway, Textract)` `Docker`
`PostgreSQL` `MongoDB` `Redis` `Celery` `Kafka` `Elasticsearch` `Loki`
`Next.js` `React` `TypeScript`

---

### Elsewhere

[LinkedIn](https://linkedin.com/in/faluyiisaiah) · faluyiisaiah@gmail.com · Lagos, Nigeria

Open to remote AI engineering work — RAG and retrieval infrastructure, document AI, evaluation infrastructure, agentic systems.
