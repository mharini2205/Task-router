# Tool guide — Claude vs ChatGPT vs Gemini vs Perplexity

Harini's paid stack is **Claude only**. So the rule is: **stay in Claude unless the task hits a specific test below.** When it does, say so *and* say whether a free tier covers it or it's worth considering paid.

## Claude — the default (paid, primary)
Best for: reasoning, writing with voice, coding, analysis, nuanced judgment, long documents, and everything wired into her plugins/skills (BYC prior-art, dossiers, paper briefs, SimNIBS setup, research toolkit). If a task doesn't clearly trip one of the tests below, the answer is Claude — then pick the model (see `model-guide.md`).

## The four "leave Claude" tests

### 1. Live web facts / citations → Perplexity
Fires when the task needs *current* information or *sourced* answers: "what's the latest on X", "find papers/news from this month", "who just published on micro-coil stimulation", quick fact-checks with links.
- Claude alone is stale (knowledge cutoff) and won't give live URLs.
- **Free tier** usually covers a few sourced answers/day. Deep Research is the paid perk.
- Workflow: **Perplexity to gather + cite → paste findings into Claude to reason/synthesize.** Don't ask Perplexity to do the hard thinking.

### 2. Enormous context / many files at once → Gemini
Fires when you want to dump *a lot* in one shot (10+ PDFs, a giant transcript, a whole dataset) and it won't sit comfortably in Claude's window.
- Gemini's context is very large and it's strong at "find X across all of this."
- **Free tier** (AI Studio / Gemini) often handles big single-shot intake.
- Workflow: **Gemini for the wide first-pass extraction → Claude for the judgment and writing.** For anything within Claude's context, skip Gemini — Claude reasons better.
- Also Gemini's edge: tight **Google Docs/Sheets/Search** integration if the work lives there.

### 3. Image generation / heavy visual layout → design tool (or ChatGPT)
Fires for making images, diagrams-as-art, or laying out a visual (a profile's look, a poster).
- For **layout/branding**: a design tool (Canva, or the Claude design MCP) — Claude writes the words, the design tool handles the look.
- For **generated images**: ChatGPT (DALL·E) free tier, or a dedicated image model.
- Text models (any Claude tier) are the wrong tool for a picture.

### 4. Second opinion / brainstorming variety → ChatGPT (free)
Fires when you want a *different* model's take to triangulate, or a wide spray of ideas fast.
- Nice-to-have, not essential. Sonnet brainstorms well on its own.
- **Free tier** is plenty for this. Only worth paid if you're using it heavily for o-series math/logic or voice.

## Quick "which tool" flow
```
Need current facts / links?        → Perplexity → back to Claude
Dumping a mountain of files?        → Gemini first-pass → back to Claude
Need an actual image / visual look? → design tool / ChatGPT(DALL·E)
Want a contrasting second opinion?  → ChatGPT (free)
Otherwise (most things)             → Claude → pick Opus/Sonnet/Haiku
```

## Honest note on cost
Since only Claude is paid, "route to Perplexity/Gemini" means *go use the free tier of that tool for that slice, then come back.* The router should only send you out when the win is real — a live-facts task or a context you physically can't fit — not for tasks Claude already does well.
