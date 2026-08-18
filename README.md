# agent-rules (FoodTruckNerdz)

This repository is the org-facing wrapper for shared agent rules.

## Layout

- `template/` â€” git submodule to `dev-centr/agent-rules` (canonical source)
- `AGENTS.md` â€” this org's thin overlay and entrypoint

## Contribution flow

- Org-specific guidance: commit in this repo
- Shared portable rules/skills: commit in `template/` and open a PR upstream to `dev-centr/agent-rules`

Do not copy the template tree into this repository.