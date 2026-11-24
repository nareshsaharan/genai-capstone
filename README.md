# Gen AI + Capstone — 4-Week Programme

Course materials, demos and projects for **Generative AI + Capstone Project**, a 4-week programme for developers with a Java / Spring Boot background. No prior AI experience needed.

> LLMs → Prompting → Claude & MCP → RAG → Agents → Local Models → Capstone

By the end you won't just *use* AI tools — you'll *build* with them at an engineering level, and ship a full-stack AI product.

## Course map

| Week | Theme | Topics | Builds |
|------|-------|--------|--------|
| [Week 1](week-1-foundations/) | Foundations & OpenAI | How LLMs work · Prompt engineering · OpenAI Java SDK · Voice & images | Voice Task Manager · Travel Planner |
| [Week 2](week-2-claude-mcp/) | Claude, MCP & Tool Use | Anthropic Java SDK · Tool use · Claude Code · MCP server | MCP Server · Claude Code App |
| [Week 3](week-3-rag-agents/) | RAG, Agents & Local Models | Embeddings · Vector stores · Agents · Ollama | RAG Study Buddy · Agent Workflow |
| [Week 4](week-4-capstone/) | Capstone | Full-stack AI app, polish & present | Full-Stack AI Study Buddy |

Four weeks. Seven builds. One full-stack AI product.

## Repository layout

```
genai-capstone/
├── week-1-foundations/   ← LLM basics, prompting, OpenAI API, voice & images
├── week-2-claude-mcp/    ← Claude API, Claude Code, tool use, MCP server in Java
├── week-3-rag-agents/    ← Embeddings, RAG with LangChain4j, agents, Ollama
├── week-4-capstone/      ← Full-Stack AI Study Buddy
├── docs/                 ← Reference notes, guides, setup help
└── slides/               ← Session decks
```

## Tech stack

| Area | What we use |
|------|-------------|
| LLMs / APIs | GPT-4o (Responses API) · Claude (Anthropic SDK, adaptive thinking) · GPT Image · Whisper · TTS |
| Java AI libraries | `openai-java` (official) · `anthropic-java` (official) · LangChain4j 1.x · Spring AI 1.x |
| RAG & vectors | LangChain4j `EmbeddingStoreIngestor` · AllMiniLmL6V2 (local) · pgvector · Chroma · Qdrant |
| MCP & agents | Spring AI MCP Server Starter · `@Tool` auto-registration · Claude Desktop / Claude Code · LangChain4j agents |
| Local models | Ollama · Llama 3.2 · Mistral · Qwen · Gemma (GGUF quantised) |
| Web / backend | Spring Boot 3.x · JDK 21 · Maven · HTML/CSS/JS frontend |

## Before you start

- **JDK 21** and **Maven**
- **Anthropic API key** (required) and **OpenAI API key** (Week 1). Budget a few dollars of credit.
- **Ollama** for Week 3 local models (optional, free)
- Keep keys in environment variables, never in code:

  ```bash
  export ANTHROPIC_API_KEY=...
  export OPENAI_API_KEY=...
  ```

- **Required reading:** Anthropic, [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) (about 15 minutes). It sets up Weeks 2–4.

## Learning outcomes

- **W1** Explain how LLMs work (tokens, embeddings, attention, sampling) and why they hallucinate.
- **W1** Write prompts that reliably produce structured output from any LLM API.
- **W2** Use Claude's adaptive thinking for hard reasoning problems via the Java SDK.
- **W2** Build and ship a Spring Boot MCP server that any MCP client can connect to.
- **W3** Build a full RAG pipeline from scratch (ingest → embed → retrieve → generate), grounded in your own data.
- **W3** Create a multi-tool AI agent with LangChain4j and run it locally with Ollama.
- **W4** Deliver a full-stack AI application (Spring Boot + Claude + RAG + JS UI) as a portfolio piece.
