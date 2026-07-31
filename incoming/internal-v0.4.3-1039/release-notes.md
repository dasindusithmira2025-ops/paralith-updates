# PARALITH Preview 0.4.3-1039

Channel: preview
Date: 2026-07-31
Git commit: 1520c28d06cc29e9915c6f3dcf667d9245446619
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
- `82b98a4d72d923948487c6b4c892a4f0f81e592ce0cf1e3c778df931ed01f48d  PARALITH.Preview_0.4.3-1039_x64_en-US.msi`
- `318809dd20c87db1bce2d2046061747162463dd80d1f2044a657513c29cbdf2e  PARALITH.Preview_0.4.3-1039_x64_en-US.msi.sig`
- `21f8e93a92e1775168369b1693c7128d29a4e0f1f357ebdaf42a0134e7b03893  PARALITH.Preview_0.4.3-1039_x64-setup.exe`
- `8dc9f5c1b6f25f7d2193fa5b6230ac15dfa83917c32cfa92f34f499b2dd344f0  PARALITH.Preview_0.4.3-1039_x64-setup.exe.sig`
