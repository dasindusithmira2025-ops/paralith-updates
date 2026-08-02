# PARALITH Preview 0.4.7-1048

Channel: preview
Date: 2026-08-02
Git commit: de5a5dfcf95a0170f34f94c6ac0a4b2eecafba01
Database schema: 27

## Highlights
- Keep automatic terminal and agent restoration inside the configured application-wide startup budget

## Fixes
- Stop workspace hydration state changes from automatically launching budget-deferred Panes
- Resume a deferred Pane only after a real user focus or Resume action
- Serialize renderer resume attempts so one interaction cannot race into multiple launches
- Prevent the Resume button from also triggering the Pane focus launch path

## Database changes
- No database schema changes
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state

## Known issues
- The recorded forced restart is Windows responding to an LSASS access violation; this release removes the remaining verified PARALITH startup load amplifier but cannot repair an independent Windows protected-process, driver, or component-store fault
- Windows component-store and protected-file verification require an elevated Administrator console
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `77ec4cc16717f6e781c015bcd3b5de7d5e1e818722effd0ff2328baf54eda62b  PARALITH.Preview_0.4.7-1048_x64_en-US.msi`
- `296d14be35240d60d07de6629190c16049d40cd1e6a2a06533fa7f81711fc9a4  PARALITH.Preview_0.4.7-1048_x64_en-US.msi.sig`
- `3aeb1150da59a723ffefbe3a2aa950b54bd09ea73bef5ba45ec6f1f16c9d1dbd  PARALITH.Preview_0.4.7-1048_x64-setup.exe`
- `aa2ac890500fd6d55cedd9e7923682f66bd8f4b7a8450aa0171fc26892e6bf9b  PARALITH.Preview_0.4.7-1048_x64-setup.exe.sig`
