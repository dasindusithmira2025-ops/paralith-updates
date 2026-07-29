# PARALITH Preview 0.4.2-1035

Channel: preview
Date: 2026-07-29
Git commit: 32619812bc91c3ac4f453df4bf46167f4e6b8b21
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
- `71d3420219dfee1c1cbca9658dffae2f4962a58a0d432a1316b6edcd5c488532  PARALITH.Preview_0.4.2-1035_x64_en-US.msi`
- `efe10112c2186dbbc607768e1fbcd8c23ae7a199887f53f738855b68f558c9cd  PARALITH.Preview_0.4.2-1035_x64_en-US.msi.sig`
- `821f1b4cf3346865c72585523150953b9c7a5dd1877b40edcf09f632eb7df43d  PARALITH.Preview_0.4.2-1035_x64-setup.exe`
- `f2df08fadd93b31f9cf8c6424b0d5e985bf5531d1d95e6b037de714d013910cc  PARALITH.Preview_0.4.2-1035_x64-setup.exe.sig`
