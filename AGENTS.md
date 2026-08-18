# FoodTruckNerdz org overlay

Primary rules source is `template/` (submodule to `dev-centr/agent-rules`).

Use this file only for org-specific overrides that should not apply globally.

When assembling context for this org's repos, resolve:

- `AGENT_RULES_PATH` = `template/` inside this wrapper (or the org clone path)
- Org overlay = this `AGENTS.md`