# 🎯 Task Router

A personal **task router & navigator** — a Claude Code plugin that, for any task you describe, tells you **which AI tool** (Claude / ChatGPT / Gemini / Perplexity) and **which Claude model** (Opus / Sonnet / Haiku) to use, optimizing for **quality vs speed vs token cost**.

Built Claude-first (that's the paid stack), so the everyday, high-value decision is **Opus vs Sonnet vs Haiku** — and it only sends you outside Claude when another tool genuinely wins.

> **Opus is a scalpel, Sonnet is your hands, Haiku is a stapler.**
> A daily doubts session is a Sonnet job, not an Opus one — Opus burns tokens fast for answers Sonnet nails. Save Opus for the moments where depth actually changes the outcome.

---

## What it does

You describe a task; it answers in one compact block:

```
🎯 Claude · Sonnet
Why: Many small back-and-forth questions — Opus wastes tokens here.
Watch: If one question turns into a hard derivation, escalate that one to Opus.
```

Examples it's tuned for:

| You're about to… | It says |
|---|---|
| Run a daily doubts session | **Claude · Sonnet** — Opus pulls more tokens for answers Sonnet nails |
| Deep-read a dense thermal-safety paper | **Claude · Opus** — understanding here changes what you build next |
| Word a patent claim | **Claude · Opus** — high stakes, precise language |
| Reformat a messy CSV | **Claude · Haiku** — mechanical, save your budget |
| Find *this month's* papers on micro-coil stimulation | **Perplexity** → then Claude to analyze (Claude alone is stale) |
| Build a profile / application | **Claude · Opus** for the core narrative *(in your own voice)* + a **design tool** for the visual layout |
| Dump 15 PDFs into one context | **Gemini** first-pass (huge context) → **Claude** to reason |

---

## Install (Claude Code)

From an interactive Claude Code session:

```bash
/plugin marketplace add mharini2205/Task-router
```

```bash
/plugin install task-router@harini-task-router
```

Then restart Claude Code if prompted. That's it.

> Installing from a local clone instead? Point the marketplace at the folder:
> `/plugin marketplace add C:/Users/Team/Task-router`

---

## How to use it

**Quick, on-demand — the `/route` command:**

```bash
/route word a patent claim for the microchannel coil array
```
```bash
/route summarize this 30-page thermal paper
```

**Hands-off — the auto-triggering skill:** just describe what you're about to do in normal chat ("I need to route my afternoon — I've got a grant paragraph and a CSV to clean"), and the `task-router` skill kicks in and routes each piece.

**As a subagent:** ask Claude to "use the router agent to decide" when you want the decision without disturbing your main thread.

---

## The routing logic (short version)

Four checks, first one wins:

1. **Needs live web facts / citations?** → leave Claude → **Perplexity**, then back to Claude.
2. **High-stakes, novel, or genuinely hard reasoning?** → **Claude · Opus**.
3. **Everyday knowledge work with some reasoning?** → **Claude · Sonnet** (the default).
4. **Fast / mechanical / high-volume-low-stakes?** → **Claude · Haiku**.

Then modifiers (huge context → Gemini; images/layout → design tool; long session → downshift to Sonnet; about to submit → one Opus polish pass).

Full detail lives in the skill's references:
- [`model-guide.md`](skills/task-router/references/model-guide.md) — Opus vs Sonnet vs Haiku + token intuition
- [`tool-guide.md`](skills/task-router/references/tool-guide.md) — Claude vs ChatGPT vs Gemini vs Perplexity + the "when to leave Claude" tests
- [`routing-matrix.md`](skills/task-router/references/routing-matrix.md) — the full task→route table

---

## Repo layout

```
Task-router/
├── .claude-plugin/
│   ├── plugin.json          # plugin manifest
│   └── marketplace.json     # makes the repo one-command installable
├── skills/
│   └── task-router/
│       ├── SKILL.md         # the decision engine (auto-triggers)
│       └── references/      # model guide, tool guide, full matrix
├── commands/
│   └── route.md             # the /route slash command
├── agents/
│   └── router.md            # the routing subagent
├── README.md
└── LICENSE
```

---

## Make it yours

The routing rules are just markdown — edit them as your habits change:

- **Add a task type:** drop a row into [`routing-matrix.md`](skills/task-router/references/routing-matrix.md).
- **Got a new paid tool?** update the stack note at the top of [`tool-guide.md`](skills/task-router/references/tool-guide.md) so it starts recommending it.
- **Disagree with a call?** change the tier in the table — the skill reads these files live.

---

## License

MIT — see [LICENSE](LICENSE).
