# AGENTS.md: NeoMetaHarness-design-system

Owns: Neo theme on Astryx, tokens, UX patterns, @neometaharness/ui guidance.

- Astryx first; a Neo component exists only when Astryx has no equivalent.
- Every pattern documents light and dark.
- Never store secrets, API keys, session tokens or private user data.

## GitHub safety circuit breaker
Follow `docs/policies/GITHUB-SAFETY-GUARDRAILS.md` and `machine/github-guardrails.json` (mode `local_only_no_actions`): no GitHub Actions, work and test locally, at most 20 GitHub writes per task, stop on 403/429 and ask a human.
