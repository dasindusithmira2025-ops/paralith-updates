# PARALITH Preview 0.4.1-1027

Channel: preview
Date: 2026-07-28
Git commit: 4bffd17279d71d772df595189c369e92df98778d
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
- `4977191319ae0810e47e8210514e27bc069ebadb2547fed796d36678aea9999d  PARALITH.Preview_0.4.1-1027_x64_en-US.msi`
- `2a9f3c4a112780b01478b3f986280dfb2c4fc844cff33bd33b285221794c5e3f  PARALITH.Preview_0.4.1-1027_x64_en-US.msi.sig`
- `db41c80dd39fa0724911d20f73837564cd38fefe3390ee595b62930195764339  PARALITH.Preview_0.4.1-1027_x64-setup.exe`
- `08458e0b85e1b88427efc582b8474c7455d6086adf5273178abcf9128554834c  PARALITH.Preview_0.4.1-1027_x64-setup.exe.sig`
