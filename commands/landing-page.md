---
description: Technical landing-page audit — speed, quality and conversion checks on a live URL
argument-hint: "[url]"
---
Run a technical landing-page audit for $ARGUMENTS.
1. Ensure `init` has been run once this session — call it first if not.
2. Resolve which account the user means (list accounts if needed).
3. Call `prompt_templates_run` with key `technical-landing-page-audit` and follow the returned prompt's [input] directives — $ARGUMENTS may already answer some of them; ask only for what is still missing.
4. Execute the analysis with HYPD's tools and deliver every output section the returned prompt asks for.

If HYPD is unavailable or not authenticated, do not fail — follow the **hypd-getting-started** skill to guide the user through connecting.
