---
description: Audit a Google Ads account, find wasted spend, or mine negative keywords. Use when the user asks to audit or review a Google Ads account, find wasted budget or efficiency losses, check what is costing money without converting, or build a negative keyword list from search terms.
---

# Google Ads account audits

Three workflows, all driven by HYPD's prompt library. Pick by what the user asked for:

| The user wants | Template key for `prompt_templates_run` |
|---|---|
| Full account audit (structure, settings, tracking, performance) | `standard-account-audit` |
| Wasted spend / efficiency losses, with the money behind each finding | `analyze-wasted-spend-efficiency` |
| Negative keyword candidates from search terms | `identify-negative-keywords` |

Steps:

1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which Google Ads account the user means (`google_ads_list_accounts` if needed; account IDs are 10 digits, dashless).
3. Call `prompt_templates_run` with the matching key and follow the returned prompt's [input] directives — the user's request may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and deliver every output section the returned prompt asks for, ranked by impact.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
