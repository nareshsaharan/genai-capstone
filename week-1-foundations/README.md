# Week 1 — Foundations & OpenAI

Master how LLMs work, craft prompts that actually control the model, and call the OpenAI API from Java, including voice and images.

## Sessions

| # | Session | Covers | In class |
|---|---------|--------|----------|
| 1 | How LLMs actually work | Tokens, embeddings, attention · Transformer intuition · The autoregressive loop · Why it hallucinates | Tokenizer playground + strawberry demo |
| 2 | Prompt engineering | Instruction clarity & delimiters · Few-shot examples · Chain-of-thought · Structured / JSON output | Prompt clinic: fix bad prompts live |
| 3 | GPT API deep dive (Java) | Official `openai-java` SDK · Responses API · Streaming & tool calling · Structured outputs as typed Java records | Streaming chat in Spring Boot |
| 4 | Conversations API | Stateful multi-turn sessions · Managing history · Persist vs stream state · Context window economics | Multi-turn Java chatbot |
| 5 | GPT Image · Whisper · TTS | Image generation · Speech-to-text · Text-to-speech · Voice loop: speak → think → reply | Voice task manager mini-project |

## Projects

### 1. AI-Powered Voice-Controlled Task Manager (sessions 3–5)

- Whisper STT: voice → text
- GPT-4o: extract task intent
- Tool calling: CRUD on tasks
- TTS: confirm the action by voice

### 2. AI-Powered Travel Planner (sessions 2–4)

- Prompt chain for preference gathering
- Function calling to external APIs
- Typed itinerary structure
- Day-by-day plan generation
