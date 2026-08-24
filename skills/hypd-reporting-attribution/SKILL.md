---
description: Build a client-ready monthly performance report, or compare GA4 attribution models (Data-Driven vs Last-Click). Use when the user asks for a monthly or client report, a performance summary for a period, or where conversion credit moves between attribution models.
---

# Reporting and attribution

| The user wants | Template key for `prompt_templates_run` |
|---|---|
| Client-ready monthly performance report (Google Ads) | `monthly-performance-report` |
| GA4 attribution comparison — Data-Driven vs Last-Click, where credit moves | `ga4-attribution-compare` |

Steps:

1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which account or GA4 property the user means (list accounts if needed).
3. Call `prompt_templates_run` with the matching key and follow the returned prompt's [input] directives — the user's request may already answer some of them; ask only for what is still missing.
4. Execute with HYPD's tools and deliver every output section the returned prompt asks for.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
