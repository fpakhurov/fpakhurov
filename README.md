# Fedor Pakhurov

I build AI systems around real workflows: retrieval, agents and local LLM inference, taken from a prototype to something measurable that runs in production. I also do research on generative models and teach generative models and NLP at the HSE Faculty of Computer Science.

[fpakhurov.com](https://fpakhurov.com/) · [Work](https://fpakhurov.com/work/) · [Notes](https://fpakhurov.com/notes/) · [CV](https://fpakhurov.com/cv/) · [LinkedIn](https://www.linkedin.com/in/fpakhurov/) · [Telegram](https://t.me/fpakhurov) · [Hugging Face](https://huggingface.co/fpakhurov)

## Production work

The code is internal; the full cases are at [fpakhurov.com/work](https://fpakhurov.com/work/).

- **Retrieval.** In the main retrieval workflow, a usable answer took about **4 minutes** per request. After rebuilding retrieval around the decision people actually make and tuning inference for latency, about **5 seconds**. [Case →](https://fpakhurov.com/work/#llm-ecommerce)
- **Local Text-to-SQL.** Moved an analytics assistant to open-weight models on one A100 inside the company perimeter. On transformers, SQL generation took **2 minutes**; on vLLM with FP8 quantization, **3 seconds**. [Case →](https://fpakhurov.com/work/#local-text-to-sql) · [Article on Habr (in Russian)](https://habr.com/ru/articles/992238/)
- **Agents.** Supply, transit and export agents under one coordinator, with a person confirming every critical operation: **5,000+** operational actions a month, estimated annual effect above **₽48M**. [Case →](https://fpakhurov.com/work/#multi-agent)

## Open projects

- **[law-links](https://github.com/fpakhurov/law-links)** — a FastAPI service that extracts legal references (`пп. 1 п. 1 ст. 374 НК РФ`) from Russian text. A second-order HMM finds the article/part/point chain, tf-idf over 18.7k law names resolves the law. F1 0.976 on a held-out test set, about 7.5 ms per text.
- **[telemetron](https://github.com/fpakhurov/telemetron)** — streaming telemetry for AI agents. Kafka → PyFlink with event-time windows that still place late, out-of-order events in the right minute → per-minute latency and tool-call metrics on a live dashboard. One command starts the stack.
- **[diffusion-hallucinations](https://github.com/fpakhurov/diffusion-hallucinations)** — can complexity–entropy features catch diffusion-model errors? They separate real from synthetic images (AUROC up to 0.86), but not hallucinations from good generations: 0 of 44 configurations were significant.
- **[fpakhurov.com](https://github.com/fpakhurov/fpakhurov.com)** — my site: work cases, research and course notes. Astro, MDX and KaTeX, fully static.

## Course notes

Courses linked by prerequisites, starting from Probability Theory. Inside each course the notes follow one line, each method answering the failure of the previous one. The NLP and Generative Models notes accompany my HSE courses.

- [Probability Theory](https://fpakhurov.com/notes/probability/) — from counting to the limit theorems, and how they become the losses, estimates and guarantees of machine learning.
- [Natural Language Processing](https://fpakhurov.com/notes/nlp/) — from tokenization and representations to Transformers, RAG and agents.
- [Generative Models](https://fpakhurov.com/notes/generative-models/) — likelihoods, latent variables, VAEs, GANs, flows and diffusion models.

## Writing and talks

- 2026 · [Generating SQL queries with local models](https://habr.com/ru/articles/992238/) — article, Habr, in Russian
- 2025 · [Evaluating hallucinations in diffusion generative models](https://cs.hse.ru/news/1092597391.html) — talk, HSE conference “AI in Mathematical Finance”
- 2025 · [Methods for evaluating generation errors of diffusion models](https://cs.hse.ru/iai/aimf/news/1073321715.html) — seminar, HSE AIM Lab, in Russian · [slides](https://cs.hse.ru/mirror/pubs/share/1101573802.pdf)

---

Python · vLLM · Hugging Face Transformers · FastAPI · Docker · Kafka · PyFlink · PostgreSQL

По-русски — [fpakhurov.com/ru](https://fpakhurov.com/ru/)
