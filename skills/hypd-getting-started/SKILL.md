---
description: Connect HYPD and your ad accounts. Use when HYPD is not connected yet, a HYPD tool returns an authentication error, or the user asks how to set up or start using HYPD.
---

# Getting started with HYPD

1. **Create a HYPD account** at https://app.hypd.ai (OAuth sign-in, no card needed to start).
2. **Connect at least one source** on the Sources page (https://app.hypd.ai/sources): Google Ads, Meta, Google Analytics, Merchant Center, Microsoft Ads, or LinkedIn Ads.
3. **Authorize the HYPD connector in your assistant.**
   - Claude Code (terminal): run `/mcp`, select **hypd**, choose **Authenticate**, approve in the browser.
   - Claude desktop app or Cowork: Settings → **Customize** → **Plugins** → open **HYPD AI - Paid Ads & Analytics** → connect the **HYPD AI Ads** connector.
   - ChatGPT: open the HYPD app's connection prompt (or Settings → **Apps** → **HYPD**) and approve in the browser.
   - An existing HYPD authorization for the same assistant account is reused automatically.
4. **Verify** with: "List my Google Ads accounts."

Full walkthrough with screenshots: https://docs.hypd.ai/guides/mcp-connector
