# PARALITH Stable 0.4.1

Channel: stable
Date: 2026-07-28
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
- `a1aa022e058c5fc0d167a646fd2f947183ae7806d88339e04fb52aea980c4c71  PARALITH_0.4.1_x64_en-US.msi`
- `61fa18c75b2f6a2386a0439da3edc199f627b9dd5e132c9ac02b30bc7f984f4e  PARALITH_0.4.1_x64_en-US.msi.sig`
- `7d9900e0beea34134faf17cad4f0233875f6bd5021105b20f262191d1e8c6f37  PARALITH_0.4.1_x64-setup.exe`
- `807d3a237ffeafcb8a968043e06c01c4b1489f093278ffeb0be592e607eb23a3  PARALITH_0.4.1_x64-setup.exe.sig`
