---
description: How to call HYPD's tools correctly — run init first, dashless account IDs, read-only guarantees, and what to do when no accounts are connected. Load before the first HYPD tool call in a session.
---

# Using HYPD's tools

Stable invariants — `init`'s output is authoritative if anything here differs:

- **Call `init` once per session before any other HYPD tool.** It returns the working context and a resolver that says which skill to load for which question. Follow it.
- **Google Ads account IDs are 10 digits, dashless** (`2712366093`, never `271-236-6093`). Get them from `google_ads_list_accounts`.
- **Everything is read-only.** No HYPD tool can create, edit, pause or delete anything in any connected platform. Never imply otherwise.
- **Cap list-style requests** (top 5/10) so responses stay fast; external research tools (keywords, SERP, ads) want a country and language.
- **No accounts returned?** The user needs to connect a source at https://app.hypd.ai/sources first.

If the HYPD MCP server is unavailable or not authenticated, do not fail — guide the user to connect: in the terminal, run `/mcp`, select **hypd**, choose **Authenticate**; in the desktop app or Cowork, open Settings → **Customize** → **Plugins** → **HYPD AI - Paid Ads & Analytics** and connect the **HYPD AI Ads** connector.
