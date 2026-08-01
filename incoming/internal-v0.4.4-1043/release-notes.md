# PARALITH Preview 0.4.4-1043

Channel: preview
Date: 2026-08-01
Git commit: 47a2df416fafecdbe23cb4d98c209f9f9af7939b
Database schema: 27

## Highlights
- Keep Browser workspaces responsive when switching tools or closing the Browser during native WebView startup
- Reveal files and folders directly in Windows Explorer from the code-surface context menu

## Fixes
- Serialize native Browser creation, visibility, and teardown so a late WebView cannot cover terminals or capture workspace input
- Hide or close cancelled Browser views after pending native creation completes
- Surface file-explorer reveal failures instead of silently discarding them

## Database changes
- No database schema changes
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state

## Known issues
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `53018c26f15306226fa6ef49734ffa1e965161add35263f31cd2ea1eb8ce4d99  PARALITH.Preview_0.4.4-1043_x64_en-US.msi`
- `5032caa45561b595fe22e978248dc26a6b3e3eddc59cefde0932d256e034d84b  PARALITH.Preview_0.4.4-1043_x64_en-US.msi.sig`
- `85aff29ae94c4965d2f31c673e596d5c041c8372214946ed9f0fec21b68efd6e  PARALITH.Preview_0.4.4-1043_x64-setup.exe`
- `ec8198d889b0ce29840a18f566d583380bdba0393d3aaa458ab3283aa1e0d5b3  PARALITH.Preview_0.4.4-1043_x64-setup.exe.sig`
