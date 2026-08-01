# PARALITH Preview 0.4.5-1044

Channel: preview
Date: 2026-08-01
Git commit: ab485cf0406716196d57f18d16fd94e9343c9fb5
Database schema: 27

## Highlights
- Bound automatic terminal restoration across all open Workspaces with one application-wide launch budget
- Publish updater assets through the protected public update repository and configured push mirror

## Fixes
- Prevent each Workspace from independently consuming the full restoration budget during startup
- Serialize concurrent Workspace restores so each restore observes the current live-session count
- Keep over-budget Panes visible as deferred instead of launching an unbounded terminal and agent burst

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
- `72eeb9c8c3dc375b6cfb069c5528fa32be328a9245e00d97fab6f875eed4da30  PARALITH.Preview_0.4.5-1044_x64_en-US.msi`
- `6fa327373cf960008e5bd5224b5eb44beedbefdcbeb7255946125e5900cafbb3  PARALITH.Preview_0.4.5-1044_x64_en-US.msi.sig`
- `994a166df3a7a2090f793009dff26404bf5e78af5e6178fdad4ca01a39548a60  PARALITH.Preview_0.4.5-1044_x64-setup.exe`
- `b783177c83049af8db928eb3716b27b7bea13c731a3e9e9a1554c00573017928  PARALITH.Preview_0.4.5-1044_x64-setup.exe.sig`
