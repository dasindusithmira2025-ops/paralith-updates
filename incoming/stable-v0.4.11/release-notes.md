# PARALITH Stable 0.4.11

Channel: stable
Date: 2026-08-12
Git commit: b7916b5b46d6ace4d57a636adbf5701929c3c730
Database schema: 28

## Highlights
- Design system revamp: a canonical design system (design.md) now governs surfaces, borders, typography, geometry, and button hierarchy across the whole application
- Reworked color, border, and typography tokens for a five-step hairline border ladder, a four-level text contrast hierarchy, and named semantic state colors (info/success/warning/danger/agent/ready/neutral)
- Buttons: only one accent-filled action per screen now — repeated per-row/per-record actions (Workspace launcher, Agent Resume) switched from primary to secondary so the dominant action stays legible

## Fixes
- Database Studio: fixed a real repository scan on a multi-package project sometimes failing with "PARALITH could not access its local database" — several identifier collisions (shared schema files, packages sharing a datasource name, repeated health issues) could abort the discovery transaction

## Database changes
- No database schema changes
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state

## Known issues
- Database Studio: Drizzle change generation is not implemented; a Drizzle-only source refuses implementation with a clear error rather than writing something wrong
- Database Studio: PostgreSQL/MySQL network introspection and any credential store remain absent by design
- A Windows protected-process, driver, or component-store fault can force a restart independently of PARALITH and cannot be repaired from within the application
- Windows component-store and protected-file verification require an elevated Administrator console
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only
- Commit history is read on demand for the selected repository or worktree; it does not refresh automatically as new commits land

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `b96c4e32ef7a010e9a7b1341289740515d6ff0f2036db14cf526ff38adaa5e98  PARALITH_0.4.11_x64_en-US.msi`
- `b8e297fb844d032d2984e4a230cae64f29a1c6a10ece9e7c3985ad05e828d74d  PARALITH_0.4.11_x64_en-US.msi.sig`
- `b3f90fd3c101058fd7040775e97546cdd5184154704dc5df8388bd72b2c12eef  PARALITH_0.4.11_x64-setup.exe`
- `731c73a3140ce13bd13742206ab57e68f84ff5a5aa4ce17036c7a090058b7891  PARALITH_0.4.11_x64-setup.exe.sig`
