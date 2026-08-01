# PARALITH Stable 0.4.5

Channel: stable
Date: 2026-08-02
Git commit: ec1cd2fe114c0b5986a3c79d93e61218d3248605
Database schema: 27

## Highlights
- Bound automatic terminal restoration across all open Workspaces with one application-wide launch budget
- Publish updater assets through the protected public update repository and configured push mirror

## Fixes
- Prevent each Workspace from independently consuming the full restoration budget during startup
- Serialize concurrent Workspace restores so each restore observes the current live-session count
- Keep over-budget Panes visible as deferred instead of launching an unbounded terminal and agent burst
- Validate protected annotated release tags against their target commit instead of the tag-object identifier

## Database changes
- No database schema changes
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state

## Known issues
- A Windows LSASS or RPC crash is an operating-system failure; this release removes PARALITH's confirmed restoration load amplifier but cannot repair an independent Windows fault
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `48ca4f89fe9fe9a90738ce6b338327c992634d1078dd89e5afbf95492d22421b  PARALITH_0.4.5_x64_en-US.msi`
- `06fdc9c704d2c2be9fd61270d690c55a105060cd0e4c036e25536c10e831c52a  PARALITH_0.4.5_x64_en-US.msi.sig`
- `f90f0f96c4eae83982d38bd9f49840c329d2398207cad9048b53675b30762d56  PARALITH_0.4.5_x64-setup.exe`
- `a30b597b381e3b5acc830f1c6ab44e0ce9fb6efb890929f554be9b465a35c5ca  PARALITH_0.4.5_x64-setup.exe.sig`
