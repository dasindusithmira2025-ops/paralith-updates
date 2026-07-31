# PARALITH Preview 0.4.4-1042

Channel: preview
Date: 2026-07-31
Git commit: 3a8518f217c4bf1adc28b07ab4ac63eb7e1ce6e5
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
- `5b9e52b920ac11e968e9ee7b83b639fa693b788ac8f11a7ae3030dda2a18a2d6  PARALITH.Preview_0.4.4-1042_x64_en-US.msi`
- `ecccd838abd449f43891a73b69d7f3f6564c659445a3f0cc8800b9e252912a96  PARALITH.Preview_0.4.4-1042_x64_en-US.msi.sig`
- `6a47b84c46b0640b185988279a29f67d5783509b1f2dae828a84a095eb8e900f  PARALITH.Preview_0.4.4-1042_x64-setup.exe`
- `9b88505bfb576599ef45b955793a56dcf859a673906885c186757b3a7fe5857b  PARALITH.Preview_0.4.4-1042_x64-setup.exe.sig`
