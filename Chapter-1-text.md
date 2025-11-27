# 📝 Chapter 1 · Text Creation

This chapter focuses on AI-assisted text creation: workflows and tool choices from ideation to final draft. Introduction-only with approaches and a curated project list—not a full tutorial.

## 💡 What AI Helps With
- Ideation and structure: topic selection, structured outlines, headings and sections
- Information synthesis: retrieval, summarization, deduplication, cross-verification
- Writing and rewriting: style transfer, tone consistency, length control
- Quality polishing: grammar/style checks, fact verification, citations
- Publishing and distribution: Markdown/docs formatting, site generation, format conversion

## ✅ Recommended Projects (by Use)

### 🖥️ Local Models and Runtimes
- [Ollama](https://ollama.com/) — run popular open-source LLMs locally (Llama, Qwen, Mistral)
- [LM Studio](https://lmstudio.ai/) — desktop model manager and chat UI
- [text-generation-webui](https://github.com/oobabooga/text-generation-webui) — rich open-source web UI
- [vLLM](https://vllm.ai/) — high-throughput inference engine for services and batch generation

### 🧩 Writing Workflows and Frameworks
- [LangChain](https://langchain.com/) (Python/JS) — orchestration and tool-calling; build writing agents quickly
- [LlamaIndex](https://www.llamaindex.ai/) — RAG and document indexing for private-source synthesis
- [Haystack](https://haystack.deepset.ai/) — clean framework for retrieval-augmented tasks

### 🧪 Prompting and Evaluation
- [promptfoo](https://promptfoo.dev/) — batch test prompts and compare models with scoring
- [Guardrails](https://www.guardrailsai.com/) — output structure constraints and safety rules (JSON/Schema)
- [TruLens](https://www.trulens.org/) / [DeepEval](https://github.com/confident-ai/deepeval) — evaluation and observability

### 📚 Documents and Publishing
- [Pandoc](https://pandoc.org/) — convert formats (Markdown/Docx/PDF/HTML)
- [Typst](https://typst.app/) — modern typesetting; lightweight LaTeX alternative
- [MkDocs](https://www.mkdocs.org/) + [Material](https://squidfunk.github.io/mkdocs-material/) — docs site generator
- [mdBook](https://rust-lang.github.io/mdBook/) — Markdown publishing for technical books/manuals

### ✍️ Grammar, Style, and Conventions
- [LanguageTool](https://languagetool.org/) — grammar/spell/style checks (multi-language)
- [Vale](https://vale.sh/) — style-guide-based text linter (great for teams)
- [Proselint](https://github.com/amperser/proselint) — English writing style checker

### 🔎 Retrieval and Vector Stores
- [Weaviate](https://weaviate.io/) / [Milvus](https://milvus.io/) — vector DBs for large-scale retrieval
- [pgvector](https://github.com/pgvector/pgvector) (PostgreSQL) — vectors inside your relational DB
- [Elasticsearch](https://www.elastic.co/) (kNN) — hybrid: traditional search + vector retrieval

### 📒 Knowledge Base and Collaboration
- [OpenWebUI](https://github.com/open-webui/open-webui) — unified chat and management UI for local/remote models
- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm) — open-source KB Q&A
- [Quivr](https://github.com/StanGirard/quivr) — second-brain style doc management and retrieval

## 🧰 Minimal Viable Stack (Low Barrier)
- Ollama + OpenWebUI: local drafting and iteration
- promptfoo: compare prompts and models
- LanguageTool: basic grammar/style checks
- Pandoc: export to target formats (Docx/PDF/HTML)

## 🚀 Advanced Stack (More Capabilities)
- vLLM: high-throughput inference service
- LlamaIndex + Weaviate: private-source RAG writing
- Vale: unify team style guides
- MkDocs (Material): generate and publish documentation sites

## 🔧 Selection Tips
- Scale and cost: individuals favor local/lightweight cloud; teams add throughput and collaboration
- Private sources: RAG raises quality; start minimal, then expand
- Evaluation first: quality comes from iteration; set up comparisons (e.g., promptfoo)
- Portability: prefer mature, general projects; avoid heavy vendor lock-in

## 🗂️ Example Workflow (Adjust as Needed)
1. Brief and outline: generate multiple outlines with local models; curate and merge
2. Research retrieval: index with LlamaIndex/Weaviate; pull key points and citations
3. Draft generation: write by modules; control length and style
4. Quality polish: run LanguageTool/Proselint; fact-check and add sources
5. Publish: convert with Pandoc; generate a site or e-book via MkDocs/mdBook

> The list favors practical, mature projects. Start with the minimal stack and swap in advanced components as you grow.

## 🙌 Support
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/A0A21P7W2J)