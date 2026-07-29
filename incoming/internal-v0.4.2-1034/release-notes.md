# PARALITH Preview 0.4.2-1034

Channel: preview
Date: 2026-07-29
Git commit: bfdbe3ae081242330e9650fa7d9102910b62286d
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
- `37e435d8b26fadffccf87671e3cbb59cd1d7fdb1be9436ab8ca4ee56133ee43a  PARALITH.Preview_0.4.2-1034_x64_en-US.msi`
- `d0504156dd807bf497aa7dfb759706359bb139a527e8c5f5045c8700d22f745e  PARALITH.Preview_0.4.2-1034_x64_en-US.msi.sig`
- `1e97f6c844dfc59446f7cb09b5febd8da6da174213f03ca9d90e4199fef9bd17  PARALITH.Preview_0.4.2-1034_x64-setup.exe`
- `09a47ae17b951dfc2a6f01d1eec9939b9afb34f565508378c078d1facc5b134a  PARALITH.Preview_0.4.2-1034_x64-setup.exe.sig`
