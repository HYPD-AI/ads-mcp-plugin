---
description: Analyze ad creatives — your own account, uploads, or competitors via the ad libraries
argument-hint: "[account, advertiser or files]"
---
Run a creative analysis for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which account the user means (list accounts if needed); Google Ads IDs are 10 digits, dashless.
3. Call `prompt_templates_run` with key `creative-analysis` and follow the returned prompt's [input] directives — $ARGUMENTS may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and present the results clearly.

If the HYPD MCP server is unavailable or not authenticated, do not fail — guide the user to connect: in the terminal, run `/mcp`, select **hypd**, choose **Authenticate**; in the desktop app or Cowork, open Settings → **Customize** → **Plugins** → **HYPD AI - Paid Ads & Analytics** and connect the **HYPD AI Ads** connector.
