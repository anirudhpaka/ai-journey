# 🌸 Phase 4 — LLMs & Transformers

**Weeks 14–17 · ~32–36 hours · Month 4**

> Full context and week-by-week table in the [main README](../README.md#-phase-4--llms--transformers).

## What lives in this folder

```
phase-4-llms/
├── week-14-transformer/       # Attention writeup + 3D walkthrough notes
├── week-15-build-gpt/         # Mini-GPT trained on Shakespeare
├── week-16-hf-ollama/         # HF pipelines + local Ollama chat
├── week-17-tool-calling/      # CLI assistant with tool calling
└── milestone-gpt-toolkit/     # 🎯 "I Built GPT" + LLM Toolkit
```

## Milestone project — "I Built GPT" + LLM Toolkit

1. **Mini-GPT from scratch** — trained on Shakespeare (or a corpus you love: song lyrics, RFCs, your Slack export). Annotated code, sample outputs, and a training curve.
2. **Tool-calling CLI assistant** — takes a question, calls 1–2 tools (web search, calculator, your local files), returns a grounded answer.

**Write the LinkedIn post:** *"I built a GPT from scratch — here's what I learned about how LLMs really work."* Recruiters notice posts like this. FDE hiring managers *especially* notice.

## Checkpoint before Phase 5

- [ ] I can explain attention in plain English
- [ ] I can explain tokens, context windows, temperature
- [ ] I can get reliable JSON out of an LLM API with a system prompt
- [ ] I can state the difference between pretraining, fine-tuning, prompting

## API cost — how to keep it near zero

- **Free tier first** — every provider has one. Google Gemini and OpenRouter (free open models) are the most generous.
- **Ollama for local** — Llama 3.1 8B and Mistral 7B run fine on a laptop with 16GB RAM. Zero cost, unlimited requests.
- **Cache aggressively** — if you're iterating on a prompt, cache the model output to disk. `functools.lru_cache` on the API call function is enough.
- **Budget** — $5–10 in credits usually covers all of Phases 4–5. Set a hard cap in the provider dashboard.

## Common gotchas

- **Tokenizer surprises** — "Learning" is 2 tokens, but " Learning" (with a leading space) is 1. Always tokenize the exact string you're going to send.
- **JSON mode ≠ valid JSON** — enable `response_format={"type": "json_object"}` when the provider supports it. Otherwise use a schema-validating library (Pydantic, Instructor).
- **System prompts have leverage** — the same model behaves 10× better with a 3-line system prompt setting persona, format, and refusals. Iterate on that first, not on the temperature.
