# Week 4 — Capstone: Full-Stack AI Study Buddy

Every concept from Weeks 1–3 comes together into one full-stack AI product. Five class sessions. Ship something real.

## Architecture

```
FRONTEND (JavaScript)          SPRING BOOT BACKEND                    AI LAYER
──────────────────────         ──────────────────────────────         ──────────────────────────
Chat UI                 REST   /api/chat        Tutor (RAG+Claude)    Claude (Anthropic)
Flashcard viewer       ─────▶  /api/flashcards  Structured cards  ──▶ LangChain4j RAG
Weak-topic heatmap             /api/progress    Weak-topic tracker    Vector store (pgvector/Chroma)
Voice input (W1)                                                      MCP server (LMS data as tools)
                               LangChain4j · Anthropic SDK · Spring AI MCP client
```

Every piece was built in a previous week. Week 4 = connect + polish + present.

## Features

| Feature | What it does | Builds on |
|---------|--------------|-----------|
| RAG-powered tutor | Claude answers from the student's own course notes, not its training memory | Week 3 RAG pipeline |
| AI flashcard generator | `POST /api/flashcards` → retrieve chunks → `List<Flashcard>` via structured output, no string parsing | Week 1 structured output |
| Weak-topic tracker | Records quiz results per topic, surfaces the weakest first, feeds the tutor's focus. Optional: served to Claude via MCP | Week 2 MCP integration |
| Voice input (optional) | Whisper STT feeds the chat box | Week 1 Whisper API |
