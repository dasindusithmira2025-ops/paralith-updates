# PARALITH Stable 0.4.6

Channel: stable
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
- `c37830c77a2e0f937b8c5916c53e8b41d8da29da03d8fc26d1a01accb34a676d  PARALITH_0.4.6_x64_en-US.msi`
- `f96ced7c749a862a41fec63ff2b2360a348eb023d7638e4f30cd70f450f7c4ae  PARALITH_0.4.6_x64_en-US.msi.sig`
- `4448a2abd16ea67ebd24e85f6b4f143a3a347069e4c3ae1838d2c271733a33d2  PARALITH_0.4.6_x64-setup.exe`
- `cd36914b1c9746729cbb3a6045f281cdef747aa00106747c26f376553dde7b71  PARALITH_0.4.6_x64-setup.exe.sig`
