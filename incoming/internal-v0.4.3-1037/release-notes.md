# PARALITH Preview 0.4.3-1037

Channel: preview
Date: 2026-07-30
Git commit: a50b439cf88b90eb16875a43d346a7a395c2f298
Database schema: 27

## Highlights
- Resume interrupted Claude Code and Codex terminals by their exact provider session ID
- Recover sessions in their original Project, repository, worktree, Workspace, and Pane context
- Review, relocate, dismiss, or resume multiple interrupted sessions from the Agent Resume Center

## Fixes
- Prevent duplicate resume launches with atomic claims and failed-pane rollback
- Reject latest-session fallbacks, unsafe provider identifiers, mismatched repositories, and invalid executable or platform boundaries
- Reconcile interrupted sessions after app restarts without copying prompts, transcripts, tokens, or environment snapshots

## Database changes
- Apply forward-only schema 27 for provider-neutral agent recovery metadata and ownership
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state during migration

## Known issues
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `ae2e6a127dfb37a66edabff1578802ff33b3bacbbbb6808094007b2acaf38911  PARALITH.Preview_0.4.3-1037_x64_en-US.msi`
- `5e1870104d39dd93e3450462c605015035cec4977ebc7da4a272fc71e2576120  PARALITH.Preview_0.4.3-1037_x64_en-US.msi.sig`
- `789ffafd1d4dfa5589894600814c8668e46f3b8965ffb85f19d6269495abda13  PARALITH.Preview_0.4.3-1037_x64-setup.exe`
- `76681ebf7fa435dd2d828f3306876e73232f478c60f9e2c8d465ca49abdcff8f  PARALITH.Preview_0.4.3-1037_x64-setup.exe.sig`
