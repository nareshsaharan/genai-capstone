# Week 2 — Claude, MCP & Tool Use

Go deeper: Claude's capabilities, the Anthropic Java SDK, Claude Code for agentic development, and building your own MCP server.

## Sessions

| # | Session | Covers | In class |
|---|---------|--------|----------|
| 1 | Fine-tuning + API mastery | Fine-tune vs RAG vs prompt · Prompt caching & Batch API · Rate limits, retries, cost control · OpenAI vs Anthropic | Cost calculator: prompt cache vs no cache |
| 2 | Claude API + Anthropic Java SDK | Official `anthropic-java` SDK · Messages, tool use, streaming · Adaptive thinking + effort control · Prompt caching in practice | Customer-support agent in Java |
| 3 | Claude Code (full walkthrough) | `CLAUDE.md` hierarchy & slash commands · Hooks (PreToolUse / PostToolUse) · Plan mode vs direct execution · Subagents & multi-file projects | Refactor a Spring Boot app with Claude Code |
| 4 | Tool use + MCP: the concept | Tools · Resources · Prompts primitives · JSON-RPC client–server · STDIO vs HTTP/SSE · The M×N integration problem | Whiteboard: MCP vs raw REST |
| 5 | Build your own MCP server in Java | Spring AI MCP server starter · `@Tool` auto-registration · Connect to Claude Desktop · The STDIO stdout trap | LMS MCP server → Claude Desktop live |

## MCP: the universal adapter

Without MCP, every app needs a custom adapter for every tool. With MCP, write the server once and any client can use it.

```
MCP client                      Your MCP server (Spring Boot)          Data
─────────────                   ─────────────────────────────          ─────────
Claude Desktop     JSON-RPC     @Tool listCourses()          calls /   LMS DB
Claude Code      ───────────▶   @Tool getAssignments()       ───────▶  Files
Your Java app    (STDIO/HTTP)   @Tool getWeakTopics()        reads     APIs
Any AI agent
```

## Projects

- **MCP Server**: an LMS MCP server in Spring Boot, connected to Claude Desktop
- **Claude Code App**: a Spring Boot app built and refactored with Claude Code
