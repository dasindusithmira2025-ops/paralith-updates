# PARALITH Preview 0.4.4-1040

Channel: preview
Date: 2026-07-31
Git commit: 4f2576c1742c48b695e35c3d6f4f0c4e686f8178
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
- `66bd5d700b6c77593fb8e8330eb52d75e76b29fa275eb703a9021d6164ada2d1  PARALITH.Preview_0.4.4-1040_x64_en-US.msi`
- `76d948bc066539979785280b24a00fd7b8ce4d0fb93cbb2d397bb42fe13e31c9  PARALITH.Preview_0.4.4-1040_x64_en-US.msi.sig`
- `b08932abf4ca62a5682209fcf6cb32b72504e43beb1559f356d619e39bbb1647  PARALITH.Preview_0.4.4-1040_x64-setup.exe`
- `371b0de497c2d341dc3fcbed1aa685e13d29cb776d10975b062d85440d882d58  PARALITH.Preview_0.4.4-1040_x64-setup.exe.sig`
