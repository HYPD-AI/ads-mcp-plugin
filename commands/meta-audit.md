---
description: Full Meta Ads account audit, tailored to ecommerce or lead-gen automatically
argument-hint: "[account] [time period]"
---
Run a Meta Ads account audit for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Resolve the Meta ad account (`meta_list_ad_accounts` if needed) and classify it as **ecommerce** or **lead-gen** from its campaign objectives and conversion setup; ask only if genuinely ambiguous.
3. Call `prompt_templates_run` with key `meta-ads-account-audit-ecommerce` or `meta-ads-account-audit-lead-gen` accordingly, then follow its [input] directives.
4. Execute with HYPD's Meta tools and deliver every output section the returned prompt asks for, ranked by impact.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
