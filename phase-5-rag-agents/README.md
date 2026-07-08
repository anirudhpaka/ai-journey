# 🟠 Phase 5 — RAG, Agents & AI Engineering

**Weeks 18–22 · ~40–45 hours · Month 5**

> Full context, RAG diagram, and week-by-week table in the [main README](../README.md#-phase-5--rag-agents--ai-engineering).

## Why this month matters

This maps **one-to-one onto AI Engineer and Forward Deployed Engineer job descriptions.** Recruiters filter for "built a RAG app with evals" faster than they filter for "trained a neural net."

## What lives in this folder

```
phase-5-rag-agents/
├── week-18-embeddings/       # 50 docs into Chroma + 10 semantic searches
├── week-19-rag-basic/        # "chat with my PDFs"
├── week-20-rag-improved/     # Reranking + eval set + before/after scores
├── week-21-agents/           # Agent with 2+ tools
├── week-22-production/       # Streaming + error handling + eval suite
└── milestone-rag-agent-app/  # 🎯 Flagship RAG + Agent App
```

## Milestone project — Production-Style RAG + Agent App (flagship)

**This is the #1 interview project.** One serious application with:

1. **Document Q&A** with citations that link back to the source chunk
2. **Agent mode** with 2+ tools (retrieval, web search, calculator, code exec)
3. **Eval suite** — at least 10 curated Q&A pairs, scored on faithfulness and relevance, with a CI-style regression report
4. **Clean UI** — Next.js if you know React, Streamlit / Gradio if you don't. Deploy it.

Pick a domain you can talk about for 10 minutes without notes. Some ideas:
- Chat with your own PDFs / notes (personal knowledge base)
- Legal case Q&A (public case law)
- Medical guideline lookup (public clinical guidelines)
- Codebase Q&A (an open-source repo you know well)

## Checkpoint before Phase 6

- [ ] I can redraw the RAG pipeline from memory in 2 minutes
- [ ] I can name 3 reasons a RAG system answers wrongly, with a fix for each
- [ ] I can explain what makes something an "agent" vs a chatbot (loop + tools + goal)
- [ ] I can describe how to evaluate an LLM app before shipping

## The 3 reasons RAG answers wrongly (memorize these)

1. **Retrieval failed** — the right chunk wasn't in the top-K. Fix: better chunking, hybrid search (dense + BM25), reranking.
2. **Retrieval succeeded but the model ignored it** — the LLM hallucinated over the context. Fix: stronger system prompt ("answer only from the context; say I don't know otherwise"), smaller context window, citations required.
3. **The docs themselves were wrong or ambiguous** — garbage in, garbage out. Fix: metadata filters, source freshness scoring, deduplication.

## Evals are not optional

If you skip the eval suite, you have not built an AI product. You have built a demo. Every serious LLM engineer says the same thing: **evals are the moat.** Ragas + a hand-curated golden set of ~10 questions is enough to start.
