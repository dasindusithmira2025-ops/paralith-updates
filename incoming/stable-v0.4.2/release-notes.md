# PARALITH Stable 0.4.2

Channel: stable
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
- `b315957725a87c045927c25413487d02298f6a7e126123f0e0e779bbab978f0d  PARALITH_0.4.2_x64_en-US.msi`
- `a94cde52f5b4745b069b112f8d1cdda55bb92a1586ce118bb0600c29e9b68903  PARALITH_0.4.2_x64_en-US.msi.sig`
- `34e928bd838b18e167efa75931fdf6184d57ceb2d1f85fd5562e8ddb191c7e86  PARALITH_0.4.2_x64-setup.exe`
- `5204fd60fbfe2f2f143d1340b54d1c6310501464aa98efe32f9f4f408b04501a  PARALITH_0.4.2_x64-setup.exe.sig`
