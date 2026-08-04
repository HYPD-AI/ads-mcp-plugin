---
description: Compare GA4 attribution models — Data-Driven vs Last-Click — and show where credit moves
argument-hint: "[property] [time period]"
---
Run an attribution comparison for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which account the user means (list accounts if needed).
3. Call `prompt_templates_run` with key `ga4-attribution-compare` and follow the returned prompt's [input] directives — $ARGUMENTS may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and deliver every output section the returned prompt asks for.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
