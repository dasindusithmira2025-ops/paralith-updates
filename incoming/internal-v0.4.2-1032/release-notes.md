# PARALITH Preview 0.4.2-1032

Channel: preview
Date: 2026-07-29
Git commit: d6d47722ad6f31389c3d2a225f989a2b604ab692
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
- `344f7cd7be5284df5589ebae6fd75b01b535e231fe852b0994204f3c1aa5f2e1  PARALITH.Preview_0.4.2-1032_x64_en-US.msi`
- `7c83b821dfa90d3efb1d747d0f294550c701cdaaa6c5c5b0ea4b2e0fbe448c59  PARALITH.Preview_0.4.2-1032_x64_en-US.msi.sig`
- `8584a537341bb653b7f79adc89181d1825574d2a75f202b3bad26830c5421fa8  PARALITH.Preview_0.4.2-1032_x64-setup.exe`
- `6764e1cf203fe2d52dd247a8038be727a0db4fc3a7d8c0163032fdd34f2a01d4  PARALITH.Preview_0.4.2-1032_x64-setup.exe.sig`
