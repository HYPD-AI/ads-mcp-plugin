---
description: Audit Merchant Center feed quality or run a technical landing-page audit. Use when the user asks about product disapprovals, Shopping feed attributes or identifiers, why products are not showing, or wants a landing page checked for speed, quality, and conversion.
---

# Shopping feed and landing pages

| The user wants | Template key for `prompt_templates_run` |
|---|---|
| Merchant Center feed quality — disapprovals, attributes, identifiers, custom labels | `mc-feed-quality-audit` |
| Technical landing-page audit — speed, quality, conversion checks on a live URL | `technical-landing-page-audit` |

Steps:

1. Ensure `init` has been run once this session — call it first if not.
2. Resolve the target: the Merchant Center account (list accounts if needed) or the exact landing-page URL including the scheme.
3. Call `prompt_templates_run` with the matching key and follow the returned prompt's [input] directives — the user's request may already answer some of them; ask only for what is still missing.
4. Execute with HYPD's tools and deliver every output section the returned prompt asks for.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
