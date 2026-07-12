# Isaiah A. Faluyi

**AI Engineer — LLM systems for messy, real-world documents.**

Most LLM projects demo beautifully and fall apart in production. I work on the ones that can't.

I build extraction pipelines that turn unstructured real-world inputs — scans, handwriting, faxes, forms — into structured, trustworthy data, and the evaluation infrastructure that proves the accuracy number is real rather than the best of five runs.

Currently: production healthcare intake automation, where a single misread character in a medical code is a total failure.

---

### What I work on

**Document AI & extraction** — OCR, handwriting, LLM extraction, layered validation and correction pipelines

**Evaluation & reliability** — golden regression suites, non-determinism handling, confidence gating, hallucination containment

**Agentic systems** — multi-agent orchestration, tool use, LLM-driven workflows

**Backend** — Python, Java, FastAPI, Django, AWS, distributed services

---

### How I think about LLM systems

A few things I've learned building extraction into a domain where being wrong has consequences:

- **A correction should never be a guess.** Every automated fix in a pipeline I build requires independent evidence — a clean copy elsewhere in the document, an explicit label, a second source agreeing at the same coordinate. Bounded, gated, unique-nearest. Otherwise you are not correcting errors, you are manufacturing confident ones.
- **Report the distribution, not the best run.** Vision models read handwriting differently every time. If your accuracy swings 88–92% run to run, the honest number is "high-80s to low-90s," not the 92 you screenshot. A single run's score is a draw from a distribution.
- **Classify failures by lever, not by symptom.** Some misses are pipeline bugs. Some are perception floors that no amount of engineering will fix. Knowing which is which is the difference between a productive quarter and a wasted one.
- **Codes are the worst possible OCR target.** No language priors, no redundancy, exact-match scoring, character-level precision. A `3` scrawled like a `5` is an unrecoverable coin flip. The leverage is structural — find the clean copy printed elsewhere — not in expecting perception to nail every glyph.

---

### Stack

`Python` `Java` `FastAPI` `Django` `Flask` `LangChain` `OpenAI` `Anthropic`
`AWS (Lambda, S3, API Gateway)` `Docker` `PostgreSQL` `MongoDB` `Redis` `Celery`
`Selenium` `BeautifulSoup` `Next.js` `TypeScript`

---

### Elsewhere

[LinkedIn](https://linkedin.com/in/faluyiisaiah) · faluyiisaiah@gmail.com · Lagos, Nigeria

Open to remote AI engineering work — document AI, evaluation infrastructure, agentic systems.
