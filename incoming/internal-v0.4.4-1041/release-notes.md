# PARALITH Preview 0.4.4-1041

Channel: preview
Date: 2026-07-31
Git commit: 9207040b4b87170144bf03f9e2f973a29b1181d9
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
- `c97bf156269a461a6461a5396720a38e73d8a598da49784fcb46b7ca64cabb07  PARALITH.Preview_0.4.4-1041_x64_en-US.msi`
- `0e6f85bd19e14b0d075c3bcc1206f81130be0804f0ac84d684a9cf261f9f6ffb  PARALITH.Preview_0.4.4-1041_x64_en-US.msi.sig`
- `5377688e22e8c83f7e071cf4a2b57f963dd246b0c9560bfea704f1fb6524b81c  PARALITH.Preview_0.4.4-1041_x64-setup.exe`
- `2253d9fef0b723a13dfb739ea7c9a6cbf98d8be62455f29e2e5ed9920a56cec8  PARALITH.Preview_0.4.4-1041_x64-setup.exe.sig`
