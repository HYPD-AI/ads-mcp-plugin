# HYPD AI - Paid Ads & Analytics

Analyze your paid marketing in plain language, inside Claude. HYPD connects your **Google Ads**, **Meta (Facebook) Ads**, **Google Analytics (GA4)** and **Merchant Center** accounts, then answers questions about them using your real account data.

**Read-only.** HYPD reports on your accounts and never changes your campaigns, budgets or ads.

## Install

```
/plugin marketplace add HYPD-AI/hypd-claude-plugin
/plugin install hypd-ai-ads@hypd-ai
/reload-plugins
```

Then run `/mcp`, select **hypd**, and authorize in your browser.

Works in **Claude Code** and **Claude Cowork**.

## What you can do

- **Google Ads** — campaign performance, spend, ROAS and CPA, account overviews, custom queries across any date range
- **Meta (Facebook) Ads** — campaign, ad set and ad performance, creative details, audience insights, catalogs, lead forms
- **Meta Ad Library** — search competitors' live and past ads across Facebook and Instagram, and view their creatives
- **Google Analytics (GA4)** — ecommerce and campaign performance, landing pages, funnels, conversion paths, attribution comparison
- **Merchant Center** — feed diagnostics, disapproved products, issue summaries, product performance, price competitiveness, competitive visibility
- **Research** — keyword ideas and search volume, competitor ads via Google Ads Transparency, live SERP and Shopping data
- **Landing pages** — instant quality audits, performance scores, resource breakdowns, screenshots
- **Prompt templates, marketing skills and saved business context**, so every answer reflects your accounts, brand and goals

Ask things like:

```
Show campaign clicks, cost, conversions and ROAS for my Google Ads account over the last 7 days.
Audit my account and tell me where budget is being wasted.
How are my Meta ads performing, and which creatives are fatiguing?
Compare attribution between Google Analytics and Google Ads.
Which of my Merchant Center products are disapproved?
Show the ads a competitor is running on Facebook and Instagram.
```

## Requirements

A HYPD account. Sign up at [app.hypd.ai](https://app.hypd.ai) and connect at least one ad account on the **Sources** page. Authentication happens over OAuth the first time you use the plugin.

## Data and privacy

- **No hooks.** This plugin registers no lifecycle hooks and observes nothing outside explicit tool calls.
- **No telemetry.** The plugin ships no analytics or tracking code. The only network destination is HYPD's own API (`mcp.hypd.ai`), reached through the MCP connection you authorize.
- **Read-only.** No tool creates, edits, pauses or deletes campaigns, budgets or ads in any connected platform.
- **Your data stays yours.** HYPD reads the advertising accounts you connect, to answer the questions you ask.

## Links

- [Website](https://www.hypd.ai)
- [Documentation](https://docs.hypd.ai)
- [Privacy Policy](https://www.hypd.ai/privacy)
- [Terms of Service](https://www.hypd.ai/terms)
- [Support](mailto:contact@hypd.ai)

## License

MIT. See [LICENSE](./LICENSE).
