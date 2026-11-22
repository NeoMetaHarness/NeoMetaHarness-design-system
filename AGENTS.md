# AGENTS.md: NeoMetaHarness-design-system

Owns: Neo theme on Astryx, tokens, UX patterns, @neometaharness/ui guidance.

- Astryx first; a Neo component exists only when Astryx has no equivalent.
- Every pattern documents light and dark.
- Never store secrets, API keys, session tokens or private user data.

## GitHub safety circuit breaker
Follow `docs/policies/GITHUB-SAFETY-GUARDRAILS.md` and `machine/github-guardrails.json` (mode `local_only_no_actions`): no GitHub Actions, work and test locally, at most 20 GitHub writes per task, stop on 403/429 and ask a human.

## Contribution protocol
Consult Astryx first. Use templates/component-spec.md for proposed UI states and interaction and templates/theme-review.md for semantic tokens, accessible focus and contrast in light/dark. Verify the implementation path through @neometaharness/ui. Route product implementation changes to the product repo.
