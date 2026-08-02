# PARALITH Preview 0.4.6-1047

Channel: preview
Date: 2026-08-02
Git commit: 95e4445a825f19dc02b619434765f2b249e183de
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
- `3d9b09ea54995d5c8e5fb4d0bc588c315121743113cc32caf37e41692600ef4b  PARALITH.Preview_0.4.6-1047_x64_en-US.msi`
- `426294bcc57a6b864986d2540c0d0c0bad6ba741e1c2c0711d6a3320c0d1cba8  PARALITH.Preview_0.4.6-1047_x64_en-US.msi.sig`
- `22e16cd4167503f64888b8f399901901ca5920dfc0efe091dd9b69679596a9dc  PARALITH.Preview_0.4.6-1047_x64-setup.exe`
- `d1a7a44c8c3acbfefe74262ff2f363fd7a7962d4024bc4ecccbe0164a0fff10c  PARALITH.Preview_0.4.6-1047_x64-setup.exe.sig`
