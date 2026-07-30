# PARALITH Preview 0.4.2-1036

Channel: preview
Date: 2026-07-30
Git commit: 868e5ab40d8cfc7a18c723646cd3f7ca12fe47aa
Database schema: 27

## Highlights
- Direct signed one-click updates with live download progress, safe-restart review, and actionable retry states
- Public artifact-only update distribution with isolated Preview and Stable channel manifests
- Project-scoped Swarm role pools with mixed Claude, Codex, and automatic runtime allocations
- Live Claude and Codex usage limits in the desktop workspace
- Exact-session recovery for interrupted Claude Code and Codex terminals
- A denser project-first sidebar and workspace information architecture

## Fixes
- Exclude only the rebuildable WebView profile from live update backups while preserving authoritative application data
- Canonicalize public release asset names so signed installer URLs remain anonymously reachable
- Normalize the repository-scoped deploy key before public updater publication
- Keep agent terminal panes from inheriting colour-suppression settings
- Serialize Swarm lifecycle operations and preserve immutable launch-time team snapshots
- Reject invalid runtime allocations and block launches when an explicitly selected runtime is unavailable

## Database changes
- Apply forward-only schemas 16-27 for orchestration, evidence, exact agent-session recovery, repository state, runtime usage, and idempotent event processing
- Backfill existing single-runtime roles and upgrade saved preset and Swarm configurations without deleting user data
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and edition-specific updater state

## Known issues
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only

## Required manual actions
- Install PARALITH Stable 0.4.1 once to bootstrap the production Stable endpoint and Stable-only verification key; later Stable releases update in-app

## SHA-256
- `fb7719f3639e872a1c552f4f260da36007d3cac8e9e92fa5a93cf4933bd6b41d  PARALITH.Preview_0.4.2-1036_x64_en-US.msi`
- `e4b5d402a84420c0d63193370d548021fc33844d94cfa1b3445d79edd2ca1947  PARALITH.Preview_0.4.2-1036_x64_en-US.msi.sig`
- `8f810c55bd91b975adc9fd90e82eeaac002f8c8cf07474aab830d52e829a1a77  PARALITH.Preview_0.4.2-1036_x64-setup.exe`
- `124a01b4d2b35ba291b36cd2268ea51dbe5dc9466f0eb618ba40e16252a00360  PARALITH.Preview_0.4.2-1036_x64-setup.exe.sig`
