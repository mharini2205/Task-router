# Claude model guide — Opus vs Sonnet vs Haiku

The everyday decision. Harini is on Claude Pro/Max, so this is where most of the value is. The goal is always **the smallest model that still does the job well.**

## One-line intuition

| Model | It is… | Reach for it when | Cost/token feel |
|-------|--------|-------------------|-----------------|
| **Opus** | the scalpel | the problem is novel, high-stakes, or genuinely hard reasoning | 💰💰💰 highest |
| **Sonnet** | your hands | everyday knowledge work — draft, code, summarize, iterate | 💰 balanced (default) |
| **Haiku** | a stapler | fast, mechanical, high-volume, low-stakes | ¢ cheapest/fastest |

## When Opus earns its cost
A wrong or shallow answer is expensive, OR the path isn't obvious. Depth here changes what you do next.
- Patent claim wording; freedom-to-operate judgment calls.
- Physics derivations you'll build on (activating function, focality vs depth, Joule-heating math).
- Reading a dense paper for *real* understanding, not a skim.
- The core narrative of a grant / SGBC application / high-stakes profile.
- Subtle debugging where the bug hides behind plausible-looking code.
- Multi-constraint planning with tradeoffs.

**Anti-pattern:** using Opus for a long back-and-forth of small questions. It's slower and burns tokens fast. Split it: reason once in Opus, iterate in Sonnet.

## When Sonnet is the right call (the default)
Most work lives here. It has strong reasoning at a fraction of Opus's token draw.
- **Daily doubts sessions** — many small turns; Sonnet nails them, Opus wastes budget.
- Drafting emails, briefs, summaries, first-pass writing.
- The majority of coding and editing.
- Re-running a known simulation setup, plugging in numbers.
- Structured extraction that needs a little judgment.
- Iterating on something Opus already framed.

**Rule of thumb:** start in Sonnet. Escalate to Opus only when Sonnet visibly struggles or the stakes justify it.

## When Haiku is enough
Speed and volume matter more than deep reasoning, and you can verify the output.
- Reformatting, reshaping tables, cleaning CSVs, renaming.
- Simple rewrites / tone tweaks on text you'll review.
- Classifying or tagging many items.
- Short factual recall you can sanity-check.
- Quick "remind me how X works" where you already half-know.

**Anti-pattern:** trusting Haiku for a judgment call or an unfamiliar fact you can't verify.

## Modifiers that pull a task sideways or up/down a tier

- **Huge input (10+ PDFs, a whole codebase dump):** if it won't fit Claude's context comfortably, consider **Gemini** for the intake/first-pass, then bring conclusions back to Claude. Otherwise stay in Claude and raise the tier one notch for synthesis.
- **Live/current facts or citations needed:** leave Claude → **Perplexity** (see tool-guide).
- **Images to generate / heavy visual layout:** a **design tool** (Canva / Claude design MCP) or ChatGPT (DALL·E), not a text model.
- **Long, iterative session:** downshift to Sonnet even if any single question could be Opus — the volume makes token cost dominate.
- **You'll act on it irreversibly (submit, publish, patent):** upshift to Opus for the final pass even if the draft was Sonnet.

## The combo move (best of both)
For a big deliverable: **draft in Sonnet, then have Opus do one focused polish pass** on the highest-stakes part (the claim, the opening paragraph, the key derivation). You get Opus quality where it matters without paying Opus rates for the whole thing.
