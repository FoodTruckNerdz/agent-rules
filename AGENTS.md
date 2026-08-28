# FoodTruckNerdz org overlay

Shared rules and Cursor skills live in **dev-centr/agent-rules**. This repo is the org overlay only - it does not vendor a snapshot.

When assembling context for this org's repos, resolve:

- `AGENT_RULES_PATH` = `$CODE_ROOT/github.com/dev-centr/agent-rules`
- Org overlay = this `AGENTS.md`

Shared changes: PR `dev-centr/agent-rules`. Org-only: commit here.

## Google Cloud (ops)

- Canonical platform project: **`food-truck-nerdz`** (display **FoodTruckNerdz Platform**, number `1084996026339`). Operator: `ryan@foodtrucknerdz.com`.
- **One platform for everything** (Gemini + OAuth consent + future Maps if needed). OAuth **clients** differentiate accessors under one consent/branding screen — e.g. **`FTN Web`**, later `FTN Android` / `FTN iOS`. Do not invent a second GCP project per app surface.
- Consent/branding on the platform project: app title **FoodTruckNerdz**, support `ryan@foodtrucknerdz.com`, authorized domain `foodtrucknerdz.com`. Prefer **External** for public site login (IAP brand create may leave Internal — flip in Auth Platform Branding if needed). Privacy/terms: `https://foodtrucknerdz.com/privacy`, `https://foodtrucknerdz.com/terms`.
- **Migration (2026-08-28):** platform consent brand exists. Live Better Auth Google login may still use web client on sibling **`ftn-app-503708`** (FTN-App, number `1008932436491`, client id prefix `1008932436491-1bmsuqctno…`) until **`FTN Web`** is created on the platform and Vercel/`FTN Google Cloud` are updated. **Do not delete** the FTN-App client until Google login is verified on `https://test.foodtrucknerdz.com`. Mark FTN-App OAuth deprecated; disable later.
- Create/apply platform web client: Console [Auth clients](https://console.cloud.google.com/auth/clients?project=food-truck-nerdz) → then `ftn-site/site-nextjs/scripts/apply-platform-oauth-client.ps1` (`-PushVercel` / `-UpdateBitwarden`). Sync helper: `scripts/sync-google-cloud-env-from-bw.ps1` (`-PushConvex`, `-PushVercel`). Never print keys/secrets.
- Gemini: Generative Language API + key **FTN Gemini API Key** on the platform project.
- Maps: web uses OpenFreeMap + Radar; Google Maps keys on GCP are legacy unless Flutter needs them.
- Multi-account gcloud login: see shared `dev-centr/agent-rules` (not duplicated here).
