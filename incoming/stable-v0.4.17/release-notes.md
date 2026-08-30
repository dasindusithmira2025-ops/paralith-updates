# PARALITH Stable 0.4.17

Channel: stable
Date: 2026-08-30
Git commit: cb268ad7cf5f554266f18ec64dd13dc45077a42a
Database schema: 40

## Highlights
- Crash fixes across the application: panic routing through the file logger so every crash leaves a reconstructable log, terminal commands moved off the Tauri event loop, and a terminal-map lock stall eliminated
- Terminal pane headers rebuilt with progressive disclosure: the resting header carries identity, and working directory, process, and agent state are one hover away without rerendering the terminal
- Run Engine and Mission Control are removed: the durable execution and orchestration surfaces shipped experimentally in 0.4.16 are gone, their tables and code deleted, and existing data preserved untouched
- Workspace canvas layout presets: named one-click layouts (tidy, grid, columns, rows) apply across docked and floating panes, with a new confirmation dialog for destructive pane-close actions

## Fixes
- Every panic is now logged with thread, location, and payload before the default hook runs, so user-reported crashes are diagnosable from the support bundle alone
- Synchronous Tauri commands were blocking the event loop; all terminal, agent, window, workspace, and project commands now run asynchronously
- A single status poll no longer stalls the entire terminal surface: session-map handles are snapshotted before cloning 64 KiB output tails, releasing the map lock before any per-session copy
- Local development builds now carry a private runtime identity so tauri dev cannot collide with an installed Stable or Preview process
- Removed dead terminal-pane CSS and the unused headless terminal constructor left behind by earlier fixes
- Visual harness ?panes=N mode now renders live sessions for every pane, matching its documented purpose

## Database changes
- Schema v40 drops the unused idx_code_refs_target index, which indexed a column that is always NULL; existing databases take a pre-migration backup before the one-statement drop and the space is reclaimed on the next vacuum
- No other schema change: all user data including projects, workspaces, terminals, swarms, memory, usage history, settings, and Stable updater state is preserved

## Known issues
- Run Engine and Mission Control tables from 0.4.16 remain in upgraded databases as orphaned data; they are never read and are preserved rather than dropped
- The Vault Markdown directory is a generated review surface; the runtime SQLite database remains the canonical source for in-app memory and evidence
- Editing generated Vault notes outside PARALITH does not yet import changes back into the runtime database
- Deep cross-file architectural inference and broad language-specific rename analysis remain intentionally conservative; ambiguous changes enter Memory review
- Usage cost is an equivalent API list-price estimate, not a provider subscription bill; models without a known rate keep their tokens visible and make the total partial
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
- `87dd57ee7abee999e2399bdf26f9459741f536b9be0e3212a9ca0f2eeeb8cc98  PARALITH_0.4.17_x64_en-US.msi`
- `226721ae92a288a5e80ac2666b7b2a99bb041778e965fe8ca38a7fc400e21e17  PARALITH_0.4.17_x64_en-US.msi.sig`
- `a9c68b06c520807fdc075b203df96d8425649c9c1d44f74bb66b7690e5112b7c  PARALITH_0.4.17_x64-setup.exe`
- `4aea7ba1f26b648df790afc369c1179f64aaeaa9d2d063c1e77ec89674a2a420  PARALITH_0.4.17_x64-setup.exe.sig`
