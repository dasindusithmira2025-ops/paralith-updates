# PARALITH Preview 0.4.6-1046

Channel: preview
Date: 2026-08-01
Git commit: 45f9324d00effec4faad9de520d0e19f216d83df
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
- `604c3dec78473b59e5114dadd3ca282675c96ad1a600156c94d763e64f8c0b07  PARALITH.Preview_0.4.6-1046_x64_en-US.msi`
- `6cf34b21dbe7279c2c2beff13e69119f5f7ef1255708dc1e0e6028108934b370  PARALITH.Preview_0.4.6-1046_x64_en-US.msi.sig`
- `bbf3d09c92cfd13d96c4497d0fdcb1d383be473ec7e3690f97e0ce64a7e1a6b4  PARALITH.Preview_0.4.6-1046_x64-setup.exe`
- `26375156bd88771be1d243fd618758a2aa447e5162e8d4cb33d0d1275ff870ea  PARALITH.Preview_0.4.6-1046_x64-setup.exe.sig`
