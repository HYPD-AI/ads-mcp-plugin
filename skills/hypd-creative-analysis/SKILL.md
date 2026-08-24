---
description: Analyze ad creatives — the user's own ads, uploaded drafts, or competitor ads from the public ad libraries (Meta, Google). Use when the user asks what ads someone is running, wants creatives described, tagged, or reviewed, or wants feedback on a draft.
---

# Creative analysis

1. Ensure `init` has been run once this session — call it first if not.
2. Resolve the source: the user's own account (list accounts if needed), uploaded files or pasted copy, or a competitor via the ad-library tools.
3. Call `prompt_templates_run` with key `creative-analysis` and follow the returned prompt's [input] directives — the user's request may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and deliver every output section the returned prompt asks for.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
