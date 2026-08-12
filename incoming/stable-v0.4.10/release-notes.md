# PARALITH Stable 0.4.10

Channel: stable
Date: 2026-08-12
Git commit: 3049123eaa9a7723327271666c30c80b7aecde3b
Database schema: 28

## Highlights
- Database Studio: redesigned schema diagram with bounded, readable table cards and real relationship-aware layout

## Fixes
- Database Studio diagram: table cards no longer grow taller than the space the layout engine reserves for them, which previously let wide tables visually overlap the node laid out below them
- Database Studio diagram: relationship lines at far/grouped zoom now connect to the visible domain boxes instead of dangling at hidden table positions

## Database changes
- Adds Database Studio persistence: sources, evidence, snapshots, objects, edges, provenance, designs, revisions, operations, layouts, and issues (schema v28)
- Existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state are preserved

## Known issues
- Database Studio: Drizzle change generation is not implemented; a Drizzle-only source refuses implementation with a clear error rather than writing something wrong
- Database Studio: PostgreSQL/MySQL network introspection and any credential store remain absent by design
- Database Studio: usage extraction is identifier-based, not a resolver; confidence is recorded per reference
- A Windows protected-process, driver, or component-store fault can force a restart independently of PARALITH and cannot be repaired from within the application
- Windows component-store and protected-file verification require an elevated Administrator console
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only
- Commit history is read on demand for the selected repository or worktree; it does not refresh automatically as new commits land

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `f0f076d2c2d5ae2eca148014256cb22d0ee56e54c364e188a924fecc9f951d18  PARALITH_0.4.10_x64_en-US.msi`
- `76742e21871d9a0b0051cb4c763623ffcc8baa9d0df043b6ce7e7fd3896a15f8  PARALITH_0.4.10_x64_en-US.msi.sig`
- `698cd597edfb1bbecf44f2ddf6dbe7f1b48d002b4c833381ecb290c84549a9f7  PARALITH_0.4.10_x64-setup.exe`
- `35aad2aa379dc4924336cc943226dcf8e76efa06dee1c4455949a4da030824c8  PARALITH_0.4.10_x64-setup.exe.sig`
