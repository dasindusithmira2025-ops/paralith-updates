# PARALITH Preview 0.4.1-1025

Channel: preview
Date: 2026-07-28
Git commit: 3fb8cb31b6e3a258a56c5296c91b08745815d073
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
- `56243b910e4b72ccf66f474e423b3b6c477483d1ac7ba2205d0d12286a1fb43d  PARALITH Preview_0.4.1-1025_x64_en-US.msi`
- `45b63a9978a454b8514153da9971e479d8eca42505335dbf70872985674943a8  PARALITH Preview_0.4.1-1025_x64_en-US.msi.sig`
- `99ff6d1294a6021f2913a633b456481131d8cbaed589948fe2e08dd306e0bb01  PARALITH Preview_0.4.1-1025_x64-setup.exe`
- `1cb7ea3ae0b31f80effcfc360969b9a9a9a057f9dc87d790088c50d1496b8cf0  PARALITH Preview_0.4.1-1025_x64-setup.exe.sig`
