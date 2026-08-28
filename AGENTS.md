# FoodTruckNerdz org overlay

Shared rules and Cursor skills live in **dev-centr/agent-rules**. This repo is the org overlay only - it does not vendor a snapshot.

When assembling context for this org's repos, resolve:

- `AGENT_RULES_PATH` = `$CODE_ROOT/github.com/dev-centr/agent-rules`
- Org overlay = this `AGENTS.md`

Shared changes: PR `dev-centr/agent-rules`. Org-only: commit here.

## Google Cloud (ops)

- Canonical platform project: **`food-truck-nerdz`** (display **FoodTruckNerdz Platform**). Operator: `ryan@foodtrucknerdz.com`.
- Sibling **`ftn-app-503708`** (FTN-App) may still hold the live OAuth web client wired to Vercel â€” do not recreate clients unless broken.
- Gemini: Generative Language API on the platform project; push via Bitwarden item **FTN Google Cloud** + `ftn-site/site-nextjs/scripts/sync-google-cloud-env-from-bw.ps1` (`-PushConvex`). Never print keys.
- Maps: web uses OpenFreeMap + Radar; Google Maps keys on GCP are legacy unless Flutter needs them.
- Multi-account gcloud login: see shared `dev-centr/agent-rules` (not duplicated here).
