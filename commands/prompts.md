---
description: Browse HYPD's full prompt library — ready-to-run analyses by category and platform
argument-hint: "[category, platform or search term]"
---
Help the user find and run a HYPD prompt template.
1. Ensure `init` has been run once this session — call it first if not.
2. Call `prompt_templates_list`, filtered by $ARGUMENTS when given (category, platform, or free-text query). Skip entries whose `runsIn` is for a different assistant.
3. Present the matches as a short grouped list of titles — never dump the raw output — and let the user pick.
4. Call `prompt_templates_run` with the chosen key and follow its [input] directives.

If the HYPD MCP server is unavailable or not authenticated, do not fail — guide the user to connect: in the terminal, run `/mcp`, select **hypd**, choose **Authenticate**; in the desktop app or Cowork, open Settings → **Customize** → **Plugins** → **HYPD AI - Paid Ads & Analytics** and connect the **HYPD AI Ads** connector.
