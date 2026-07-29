# PARALITH Preview 0.4.1-1030

Channel: preview
Date: 2026-07-29
Git commit: 9989f9601de99ab8bf09b1ec97824e082db6d56c
Database schema: 26

## Highlights
- Direct signed one-click updates with live download progress, safe-restart review, and actionable retry states
- Public artifact-only update distribution with isolated Preview and Stable channel manifests
- Role pools that combine Claude, Codex, and automatic runtime allocations within one Swarm role
- Allocation-aware Swarm staffing with stable worker provenance across persistence and restart
- A dense team editor for adding, removing, sizing, and duplicating mixed-runtime role pools

## Fixes
- Move executable updater payloads off Firebase Spark while retaining a JSON-only bridge for installed Preview 0.4.1-1023 builds
- Keep Preview publication automatic after validated main merges while Stable remains protected-tag only
- Reject duplicate runtime allocations, empty enabled roles, negative counts, and teams above the capacity limit
- Block Swarm launch with actionable errors when an explicitly selected runtime is unavailable
- Preserve immutable launch-time team snapshots when source presets are edited later

## Database changes
- Add forward-only schemas 16-20 for role allocations, lifecycle history, runtime sessions, evidence, reviews, recovery, worktrees, file ownership, tests, command drafts, project Memory context, repair lineage, and idempotent runtime-event receipts
- Backfill existing single-runtime roles and upgrade saved preset and Swarm configurations without deleting user data
- Add forward-only schema 25 for read-only AI usage snapshots and safe incremental scanner checkpoints

## Known issues
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote synchronization is explicit-refresh only; native repository watching and background event-relay synchronization are not included
- Live cross-repository publication remains blocked until administrators provision the narrowly scoped PARALITH_UPDATES_TOKEN in each release environment

## Required manual actions
- None

## SHA-256
- `dac89c408979be52be16589068822e14e5c22f45708e6a1f705a272f9ed6dd12  PARALITH.Preview_0.4.1-1030_x64_en-US.msi`
- `c683651e92c3c5ccb31da5f4c167a648000e5a4f45babfff4c7440126282a46f  PARALITH.Preview_0.4.1-1030_x64_en-US.msi.sig`
- `1981cda33ac48b3e7d4e0bed8ba4f6330f132c351fbce615c50c30af7167e319  PARALITH.Preview_0.4.1-1030_x64-setup.exe`
- `a97c7eca6dd99340f817988bc888022b1677f9dc3827a6feee109d426695551d  PARALITH.Preview_0.4.1-1030_x64-setup.exe.sig`
