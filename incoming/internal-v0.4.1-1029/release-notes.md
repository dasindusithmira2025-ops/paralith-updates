# PARALITH Preview 0.4.1-1029

Channel: preview
Date: 2026-07-28
Git commit: 05fe60bcfaceede8b99172f9a1a3e3e73aaca96e
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
- `c221a1f1a07fe63935d579d0d5887d722e5a86ec07ee317e66c0cfe2868f6e01  PARALITH.Preview_0.4.1-1029_x64_en-US.msi`
- `8f5f3d6e13d2e7a59b6e3162e6c112911b9e5310d9eea7e435c4a2679b7d78c2  PARALITH.Preview_0.4.1-1029_x64_en-US.msi.sig`
- `448868e0f63a92aa7c307b2d48c76e82c2ac63240b69b21b9e2ba2a34982dd1c  PARALITH.Preview_0.4.1-1029_x64-setup.exe`
- `0f2907195f7c423127751347c50766c7cbbfc3ed589d4e3e04af24499897c586  PARALITH.Preview_0.4.1-1029_x64-setup.exe.sig`
