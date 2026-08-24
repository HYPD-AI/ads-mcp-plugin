---
description: Keyword research with real volumes and CPCs — for a new search campaign or to expand an existing one. Use when the user asks for keyword ideas, search volumes, keyword gaps, or keywords for a campaign or market.
---

# Keyword research

1. Ensure `init` has been run once this session — call it first if not.
2. Determine whether this is for a **new** campaign or **expanding an existing** one — a named existing campaign means expansion; ask one quick question only if genuinely ambiguous.
3. Call `prompt_templates_run` with key `keyword-research-for-a-new-search-campaign` (new) or `keyword-expansion-for-an-existing-search-campaigns` (existing), then follow its [input] directives. Research tools want a country and language — ask if the market is unclear.
4. Execute with HYPD's research tools and present keywords with volumes grouped by intent.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
