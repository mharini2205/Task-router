# Full routing matrix

Match the incoming task to the nearest row. `Route` is the primary pick; `Combo` is the better move when a deliverable has parts.

## Research & reading

| Task | Route | Combo / note |
|------|-------|--------------|
| Daily doubts / quick Q&A session | Claude · **Sonnet** | Many small turns; Opus wastes tokens |
| Deep-read a dense biophysics/thermal paper | Claude · **Opus** | Understanding here changes next steps |
| TL;DR / 1-paragraph summary of a paper | Claude · **Sonnet** | **Haiku** if it's a clean abstract |
| Multi-paper synthesis / comparison table | Claude · **Sonnet** → **Opus** for the "so what" | Sonnet extracts, Opus judges the gap |
| "What's the latest on X" / find recent papers | **Perplexity** → Claude | Claude is stale for current work |
| Explain a concept you sort of know | Claude · **Sonnet** | Haiku if you just need a refresher |

## Physics / simulation (BYC)

| Task | Route | Combo / note |
|------|-------|--------------|
| Derivation you'll build on (activation, focality, heating) | Claude · **Opus** | Correctness compounds |
| Re-run a known SimNIBS/COMSOL setup, plug numbers | Claude · **Sonnet** | Use the simnibs-tms-setup skill |
| Interpret a sim log / GUI error | Claude · **Sonnet** | Opus only if it's genuinely puzzling |
| Look up tissue σ / εᵣ values | Claude · **Haiku** | Then verify against a source |
| Design a new model / novel approach | Claude · **Opus** | Ambiguous + high-stakes |

## IP / prior-art

| Task | Route | Combo / note |
|------|-------|--------------|
| Patent claim wording | Claude · **Opus** | Precision + stakes |
| Freedom-to-operate judgment call | Claude · **Opus** | Wrong answer is expensive |
| Prior-art *scoping* with live links | **Perplexity** → Claude to map | Use byc-prior-art-map skill after |
| Add references to an existing mapper | Claude · **Sonnet** | Mechanical-ish once found |
| Verify an inventor/author identity | Claude · **Sonnet** (+ Perplexity for live sources) | |

## Writing & applications

| Task | Route | Combo / note |
|------|-------|--------------|
| Profile/application — **core narrative** | Claude · **Opus** + your own voice | Your words lead; Opus for structure/edge cases |
| Profile/application — **visual layout** | **Design tool** (Canva / Claude design MCP) | Claude for words, design for look |
| First draft of an email / blurb | Claude · **Sonnet** | Opus only for a high-stakes send |
| Polish a final paragraph before submitting | Claude · **Opus** (one pass) | Draft was Sonnet; Opus for the last mile |
| Tone tweak / shorten text you'll review | Claude · **Haiku** | Mechanical |

## Mechanical / data

| Task | Route | Combo / note |
|------|-------|--------------|
| Reformat/reshape a table, clean a CSV | Claude · **Haiku** | Fast + cheap |
| Rename / bulk find-replace / tag items | Claude · **Haiku** | |
| Structured extraction needing judgment | Claude · **Sonnet** | Haiku if the source is clean |
| Dump 10+ PDFs into one context | **Gemini** first-pass → Claude | Only if it won't fit Claude |

## Meta

| Task | Route | Combo / note |
|------|-------|--------------|
| "Which model should I use for this?" | this router (any tier) | That's the whole point |
| Brainstorm many varied angles | Claude · **Sonnet** | ChatGPT free for a contrasting spray |
| Second opinion to triangulate | **ChatGPT (free)** | Nice-to-have |

## Escalate / downgrade triggers (say these out loud when routing)
- Sonnet visibly struggling or hedging → **escalate to Opus.**
- A long session of small questions → **downgrade to Sonnet** even if any one Q could be Opus.
- Output is mechanical and verifiable → **downgrade to Haiku.**
- Task needs a fact after your knowledge cutoff → **leave Claude → Perplexity.**
- You're about to submit/publish/patent → **one Opus pass on the final.**
