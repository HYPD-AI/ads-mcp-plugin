---
description: Audit Merchant Center feed quality — disapprovals, attributes, identifiers, custom labels
argument-hint: "[merchant account]"
---
Run a Merchant Center feed quality audit for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which account the user means (list accounts if needed).
3. Call `prompt_templates_run` with key `mc-feed-quality-audit` and follow the returned prompt's [input] directives — $ARGUMENTS may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and deliver every output section the returned prompt asks for.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
