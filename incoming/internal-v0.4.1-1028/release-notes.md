# PARALITH Preview 0.4.1-1028

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
- `0471bfa28c9ecf21c4133f0d6b73bab1fe431c0279e17e421b1e06cc50277f54  PARALITH.Preview_0.4.1-1028_x64_en-US.msi`
- `c6d77b1cacd956e62d7f9c3b88e701665be83f12d90d37161764c4cf5f4c5850  PARALITH.Preview_0.4.1-1028_x64_en-US.msi.sig`
- `0a4f4233d8f3a94100792766a9da64dd9845468c8ca49f457c2e5e7a00baaf1a  PARALITH.Preview_0.4.1-1028_x64-setup.exe`
- `0b4e8d1728fc473f849cb98214c8eba704aea945f12f942da8e27d52c208a3e1  PARALITH.Preview_0.4.1-1028_x64-setup.exe.sig`
