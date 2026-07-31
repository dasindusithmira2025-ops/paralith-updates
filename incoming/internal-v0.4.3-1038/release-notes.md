# PARALITH Preview 0.4.3-1038

Channel: preview
Date: 2026-07-31
Git commit: 4a495d2746ced977e3b1c1666c87fbecf35b7b3c
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
- `de2d1cc70fadb240fcf65231afd11240092c3ae4bb3f4d8a44d3e8cf0c2ac801  PARALITH.Preview_0.4.3-1038_x64_en-US.msi`
- `1d48f1cd27d5ce0ca486e853212d3f23cc999d84815469a5ee9de8a5073082fa  PARALITH.Preview_0.4.3-1038_x64_en-US.msi.sig`
- `8436c95456ac73438ca7ab35829a5c29197eab8920bfe551ee8b64e11948aa68  PARALITH.Preview_0.4.3-1038_x64-setup.exe`
- `933e6d9f5fe7bc1afa84f278acc7dd900338504cdbf8c7f823086efc97d8c148  PARALITH.Preview_0.4.3-1038_x64-setup.exe.sig`
