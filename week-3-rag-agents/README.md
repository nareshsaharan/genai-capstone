# Week 3 — RAG, Agents & Local Models

Build a RAG pipeline from scratch in Java, create an agent that uses tools, and run powerful models locally with Ollama, for free.

## Sessions

| # | Session | Covers | In class |
|---|---------|--------|----------|
| 1 | Embeddings & vector databases | Semantic meaning as coordinates · Cosine similarity & nearest neighbours · In-memory → Chroma → pgvector · Choosing a store for prod | Nearest-neighbour search demo |
| 2 | RAG pipeline in Java (LangChain4j) | Ingest: load → chunk → embed → store · Retrieve: embed query → top-k · Augment: inject chunks as context · Generate: grounded, citation-ready answers | RAG over course notes, live Q&A |
| 3 | AI agents & agentic workflows | `AiServices` + `@Tool` in LangChain4j · Orchestrator–worker patterns · Agents vs workflows · Error handling in multi-step loops | Research agent that searches + summarises |
| 4 | Running & deploying local models | Ollama: pull & run GGUF models · Llama 3, Mistral, Gemma, Qwen · Same LangChain4j code, swap one bean · Q4 vs Q8 quantisation | Local RAG with Ollama + Llama, no API key |

## The RAG pipeline

Run ingestion once. Run retrieval for every user question.

```
① Ingestion (once)        Load ──▶ Chunk (~300 tokens) ──▶ Embed ──▶ Store (Chroma / pgvector)

② Per query               Embed query ──▶ Search top-k ──▶ Augment prompt ──▶ Generate answer
```

Result: grounded, citation-ready answers from *your* data, not the model's training memory.

## Projects

- **RAG Study Buddy**: Q&A over course notes with LangChain4j
- **Agent Workflow**: a multi-tool research agent, runnable locally with Ollama
