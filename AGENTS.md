# AGENTS.md

This repository is docs-first and orchestrator-first.

## Source of truth

- `docs/AGENTS.md`
- `docs/README.md`
- `docs/00-context/*`
- `docs/01-product/prd.md`
- `docs/02-work-items/backlog.md`
- `docs/03-logs/*`
- `docs/04-process/*`
- `.agents/skills/README.md`

## Autonomy model

- Human defines context and validates implementation kickoff.
- Orchestrator executes the implementation loop autonomously after kickoff.
- Coder/reviewer/autofix roles run within explicit scope and contracts.
- No mandatory human checkpoint between dispatch/revise/complete.

## Operating rules

- Keep diffs focused and minimal.
- Always list executed commands and summarize results.
- Ask for missing context instead of guessing.
- No mandatory ticket system.
- Follow: Context -> Plan -> Dispatch -> Validate -> Finalize.
- Coder agents do not edit `docs/03-logs/*`.

## Safety and quality

- Deterministic checks run first.
- Codex fallback auto-fix is allowed on scoped files only.
- Out-of-scope edits are blocked by `tools/scope-guard`.
- Use `tools/offload-proxy/pp` for heavy command output.

## Risk authority

- Human approval is required only for destructive/high-risk actions.
