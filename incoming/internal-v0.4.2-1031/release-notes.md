# PARALITH Preview 0.4.2-1031

Channel: preview
Date: 2026-07-29
Git commit: 102cfc6dbbf0556a0d4d4a6614c0e25edf989e16
Database schema: 26

## Highlights
- Direct signed one-click updates with live download progress, safe-restart review, and actionable retry states
- Public artifact-only update distribution with isolated Preview and Stable channel manifests
- Project-scoped Swarm role pools with mixed Claude, Codex, and automatic runtime allocations
- Live Claude and Codex usage limits in the desktop workspace
- A denser project-first sidebar and workspace information architecture

## Fixes
- Exclude only the rebuildable WebView profile from live update backups while preserving authoritative application data
- Canonicalize public release asset names so signed installer URLs remain anonymously reachable
- Normalize the repository-scoped deploy key before public updater publication
- Keep agent terminal panes from inheriting colour-suppression settings
- Serialize Swarm lifecycle operations and preserve immutable launch-time team snapshots
- Reject invalid runtime allocations and block launches when an explicitly selected runtime is unavailable

## Database changes
- Apply forward-only schemas 16-26 for orchestration, evidence, recovery, repository state, runtime usage, and idempotent event processing
- Backfill existing single-runtime roles and upgrade saved preset and Swarm configurations without deleting user data
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and edition-specific updater state

## Known issues
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only

## Required manual actions
- Install PARALITH Stable 0.4.1 once to bootstrap the production Stable endpoint and Stable-only verification key; later Stable releases update in-app

## SHA-256
- `007e23008085c803b183f22c8b054fc24760e535a3a7ae17bf0a080f056328e6  PARALITH.Preview_0.4.2-1031_x64_en-US.msi`
- `2b9bcf7a598c78bb5743b4c179733e1fad3fafaf477c828d240bdb6080f6c9ee  PARALITH.Preview_0.4.2-1031_x64_en-US.msi.sig`
- `7267b777aca0277a218345e5677744b881af0c1d7b4deba02a00e96e97b35608  PARALITH.Preview_0.4.2-1031_x64-setup.exe`
- `9d0487d8bc095878ed474dbdc886bcbfb4171f4a884b044d70cccbc447166cb7  PARALITH.Preview_0.4.2-1031_x64-setup.exe.sig`
