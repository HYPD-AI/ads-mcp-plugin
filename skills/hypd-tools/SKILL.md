---
description: How HYPD's tools work and the invariants to respect when calling them. Load before the first HYPD tool call in a session.
---

# Using HYPD's tools

Stable invariants — `init`'s output is authoritative if anything here differs:

- **Call `init` once per session before any other HYPD tool.** It returns the working context and a resolver that says which skill to load for which question. Follow it.
- **Google Ads account IDs are 10 digits, dashless** (`2712366093`, never `271-236-6093`). Get them from `google_ads_list_accounts`.
- **Everything is read-only.** No HYPD tool can create, edit, pause or delete anything in any connected platform — state only what the data shows; HYPD itself never took an action.
- **Cap list-style requests** (top 5/10) so responses stay fast; external research tools (keywords, SERP, ads) want a country and language.
- **No accounts returned?** Follow the **hypd-getting-started** skill — the user needs to connect a source first.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
