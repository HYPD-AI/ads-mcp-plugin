---
description: Keyword research — for a new search campaign or to expand an existing one, with volumes and CPCs
argument-hint: "[topic or campaign] [market]"
---
Run keyword research for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Determine whether this is for a **new** campaign or **expanding an existing** one — infer from $ARGUMENTS (a named existing campaign means expansion); ask one quick question only if genuinely ambiguous.
3. Call `prompt_templates_run` with key `keyword-research-for-a-new-search-campaign` (new) or `keyword-expansion-for-an-existing-search-campaigns` (existing), then follow its [input] directives.
4. Execute with HYPD's research tools and present keywords with volumes grouped by intent.

If the HYPD MCP server is unavailable or not authenticated, do not fail — guide the user to connect: in the terminal, run `/mcp`, select **hypd**, choose **Authenticate**; in the desktop app or Cowork, open Settings → **Customize** → **Plugins** → **HYPD AI - Paid Ads & Analytics** and connect the **HYPD AI Ads** connector.
