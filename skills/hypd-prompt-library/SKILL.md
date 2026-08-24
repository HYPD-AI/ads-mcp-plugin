---
description: Browse HYPD's library of 87+ ready-to-run ad analyses. Use when the user asks what analyses HYPD offers, wants to explore available reports or audits by platform or category, or asks for an analysis no other skill covers.
---

# The HYPD prompt library

1. Ensure `init` has been run once this session — call it first if not.
2. Call `prompt_templates_list`, filtered by the user's request when given (category, platform, or free-text query). Skip entries whose `runsIn` is for a different assistant.
3. Present the matches as a short grouped list of titles — never dump the raw output — and let the user pick.
4. Call `prompt_templates_run` with the chosen key and follow its [input] directives.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
