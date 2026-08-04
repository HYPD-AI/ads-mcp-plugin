---
description: Find wasted Google Ads spend and efficiency losses, with the money behind each finding
argument-hint: "[account] [time period]"
---
Run a wasted-spend analysis for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which account the user means (list accounts if needed); Google Ads IDs are 10 digits, dashless.
3. Call `prompt_templates_run` with key `analyze-wasted-spend-efficiency` and follow the returned prompt's [input] directives — $ARGUMENTS may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and present the results clearly.

If the HYPD MCP server is unavailable or not authenticated, do not fail — guide the user to connect: in the terminal, run `/mcp`, select **hypd**, choose **Authenticate**; in the desktop app or Cowork, open Settings → **Customize** → **Plugins** → **HYPD AI - Paid Ads & Analytics** and connect the **HYPD AI Ads** connector.
