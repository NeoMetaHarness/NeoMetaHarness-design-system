# GitHub Safety Guardrails

These rules are binding for every NeoMetaHarness agent and contributor. The machine-readable form is `machine/github-guardrails.json`, and `pnpm check` enforces it. The rules are inherited from the BrowserHarness org (user decision).

## Operating model
GitHub is for source control and collaboration only, not compute.
- **No GitHub Actions and no workflows.** Never create or change `.github/workflows/*`. Tests, builds, linting, evals and upstream syncs all run locally.
- **Work locally, sync in batches.** Commit locally, then push or pull once a unit of work is done. Never write files through the API one call at a time.
- Agents, schedulers, model inference and automation run on Neo nodes, never on GitHub.

Mode: `local_only_no_actions`. Only the user can change it.

## Circuit breaker
If GitHub returns a 403 or 429 about restriction, suspension, abuse controls or rate limiting:
1. Stop all GitHub writes and automatic retries.
2. Record the exact error.
3. Don't work around it (no other accounts, orgs, runners or workflows).
4. Keep working and committing locally.
5. Get human approval before resuming GitHub writes.

## Bulk limits
- At most 20 GitHub write operations per task (a push counts as one).
- Changing more than 3 repositories in one task needs human approval.
- No automated starring, following, comment spam or bulk repo creation.

## Needs explicit human approval
Workflows, schedules, runners, workflow secrets, Pages for production, guardrail changes, and any exception. An agent can't approve its own exception.

## Resilience
Source must never live only on GitHub. Keep a local clone of every repo with full history.
