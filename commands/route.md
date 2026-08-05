---
description: Recommend the best AI tool + Claude model (Opus/Sonnet/Haiku) for a task, optimizing quality vs speed vs token cost.
argument-hint: <describe the task you're about to do>
---

Use the **task-router** skill to route this task: **$ARGUMENTS**

Follow the skill's decision procedure. Respond in the compact format:

```
🎯 <Tool> · <Model>
Why: <one line>
Watch: <optional — token cost / downgrade trigger>
```

If a deliverable has parts (e.g. words + visuals, or draft + final polish), add one line suggesting the **combo**. If the task is ambiguous about what makes it hard, ask exactly one clarifying question first, then route. Keep it short and opinionated — Claude-first, but flag when Perplexity/Gemini/a design tool genuinely wins.
