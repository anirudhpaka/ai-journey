# 🟩 Phase 6 — Deploy, Portfolio & Interview Prep

**Weeks 23–26 · ~30–34 hours · Month 6**

> Full context and week-by-week table in the [main README](../README.md#-phase-6--deploy-portfolio--interview-prep).

## The month's mindset shift

Weeks 1–22 were about **learning**. Weeks 23–26 are about **evidence**. Everything you do now is aimed at one question a hiring manager will ask:

> *"Show me something you built and walk me through it."*

## What lives in this folder

```
phase-6-deploy/
├── week-23-fastapi-docker/   # Dockerfile + FastAPI wrapper for RAG app
├── week-24-deploy/           # HF Spaces / Vercel configs
├── week-25-portfolio/        # Architecture diagrams, demo GIFs, writeups
├── week-26-interviews/       # Study notes, mock interview scripts
└── graduation/               # 🎓 The Job-Ready Package
```

## Milestone project — 🎓 The Job-Ready Package

By end of Week 26:

- **3 deployed projects with public URLs** — the flagship RAG app + 2 more (image classifier, mini-GPT)
- **A GitHub that tells a 6-month story** — clear README arc, pinned repos, commit history that shows steady progress
- **2 technical posts** — LinkedIn or Dev.to. One "here's how I built the flagship." One "here's what I learned about [attention / RAG / evals]."
- **An AI-focused resume** — highlight the projects, not the courses
- **Practiced interview answers** — 20 questions answered aloud, 2 mock interviews

That is not "learning AI." That is **being an AI engineer.**

## Deploy checklist (per project)

- [ ] Public URL that works on mobile
- [ ] Loading states — never a blank screen
- [ ] Error handling — user sees "something went wrong" not a stack trace
- [ ] Rate limit or auth so a stranger can't drain your API credits
- [ ] README with: what it is, a demo GIF, architecture diagram, how to run locally, tech stack
- [ ] Environment variables in `.env.example`, secrets in the host's secret manager

## Resume format that works for AI Engineer / FDE roles

```
[Name] — AI Engineer
[email] · [github.com/you] · [linkedin] · [portfolio URL]

PROJECTS  (put these ABOVE experience if you're career-switching)

▸ [Flagship RAG App Name] — flagship LLM app with citations, agent tools, eval suite
  • Built RAG pipeline (Chroma, hybrid search, reranking) that improved
    faithfulness from 62% to 91% on a 40-question golden set.
  • Deployed as FastAPI + Next.js on Vercel + HF Spaces. Handles ~200 QPD.
  • [URL] · [GitHub]

▸ [Second project] — ...
▸ [Third project] — ...

EXPERIENCE  (recent, senior work first)
...

EDUCATION  (short)
```

## Interview questions to nail

**ML fundamentals**
- Explain bias / variance tradeoff
- Precision vs recall — when to prefer each
- Why do we split into train/val/test?
- What is regularization and why does it work?

**LLM system design**
- Design a RAG system for [customer support / legal / medical]
- How do you evaluate an LLM app before shipping?
- What are your cost/latency levers?
- How would you build an agent that [does X]?

**Behavioral**
- Walk me through a project — start with the problem, not the tech
- What went wrong on a project and what did you learn?
- Why AI Engineer / why now?

**Practice out loud, not in your head.** Record yourself. It's uncomfortable and it's the fastest way to get better.
