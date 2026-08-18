# agent-rules (FoodTruckNerdz)

Org overlay for agent rules. Shared portable rules and Cursor skills are **not** copied here - a git submodule would pin a SHA and go stale.

Canonical: https://github.com/dev-centr/agent-rules

Clone or fetch that repo (`$CODE_ROOT/github.com/dev-centr/agent-rules`). Junction skills from there into `~/.cursor/skills/<name>/`.

## Layout

- `AGENTS.md` - this org's overlay (ORG, docs host, forge quirks)

## Contribution flow

- Org-specific guidance: commit in this repo
- Shared rules/skills: PR https://github.com/dev-centr/agent-rules