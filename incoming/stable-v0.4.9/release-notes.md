# PARALITH Stable 0.4.9

Channel: stable
Date: 2026-08-10
Git commit: 184a21cd8c535f30ecbf55af83d1ff726e5f2b56
Database schema: 27

## Highlights
- Start PARALITH without repeated console windows flashing while saved agent sessions are checked

## Fixes
- Run startup Git repository probes as hidden background processes on Windows
- Apply the same hidden-process rule to repository history and terminal-session persistence Git probes

## Database changes
- No database schema changes
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state

## Known issues
- A Windows protected-process, driver, or component-store fault can force a restart independently of PARALITH and cannot be repaired from within the application
- Windows component-store and protected-file verification require an elevated Administrator console
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only
- Commit history is read on demand for the selected repository or worktree; it does not refresh automatically as new commits land

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `cc87f2765c7b5e7c0f9e0465b4f7acda50f572e0ba09d7aefb73f0433e9cebc1  PARALITH_0.4.9_x64_en-US.msi`
- `9e6be8038ae67bea5589bb57da0ff40b7ca1e80981be9c7c90e863233a3ffb37  PARALITH_0.4.9_x64_en-US.msi.sig`
- `7ddde5dbdad3a0cfa8baf72a2296180b38557fb5cebc1a766775559722708f6d  PARALITH_0.4.9_x64-setup.exe`
- `9da7a3fc9c037846033559e5d68db9eae0511ed4d23176507c8b487c1005c488  PARALITH_0.4.9_x64-setup.exe.sig`
