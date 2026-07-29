# PARALITH Preview 0.4.2-1033

Channel: preview
Date: 2026-07-29
Git commit: 3a86c8d808e2497433c672fc95d5aef1e16637df
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
- `6de9a69fef0a80b2ed3193c29ec94d4e6dcab09ba4241ff869bbe14a7056bc26  PARALITH.Preview_0.4.2-1033_x64_en-US.msi`
- `8db3f424512c74eca8be52e4f8e256f666e2f9f6bb4a2e818a6903a37ed1e2e5  PARALITH.Preview_0.4.2-1033_x64_en-US.msi.sig`
- `eb364e5136b35a35319f5287da57169a0d7c0f3f0ddab0349b6a94f7082861cb  PARALITH.Preview_0.4.2-1033_x64-setup.exe`
- `822d42bd468ed8185fadbd377f7df216e04ed0fee4a3d193fa92c45181f11d56  PARALITH.Preview_0.4.2-1033_x64-setup.exe.sig`
