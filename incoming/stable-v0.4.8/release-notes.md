# PARALITH Stable 0.4.8

Channel: stable
Date: 2026-08-10
Git commit: 7374a1e13a3e4ad0ec2144ed8960d684c9a6885b
Database schema: 27

## Highlights
- Browse a repository's commit history inside the Repository Command Center without leaving PARALITH
- Open any commit to read its metadata and the files it changed
- Read history for a selected worktree, not only the primary checkout
- Show live terminal and agent state for every open Project in the sidebar, not only the Project currently on screen
- Surface Workspaces whose agents are waiting on a person, and rank them first under the Needs you order
- List only the Projects being worked in, so a Project opened once months ago no longer occupies the sidebar
- Persist sidebar grouping, order, and collapsed sections in application settings so every window agrees

## Fixes
- List commits touching paths that contain spaces, quotes, or newlines instead of truncating them
- Report a renamed file with both its old and new path rather than an empty entry
- Show binary files as binary instead of reporting a line count they do not have
- Stop a background Project's row reporting terminals as running after they have exited
- Report Workspaces blocked on input or a permission prompt as waiting instead of active
- Mark terminal sessions that ended while the application was not listening as exited rather than leaving them running
- Clear a Workspace's agent state when its terminals are stopped, so it cannot keep requesting attention
- Hold the sidebar order steady while a row is dragged or its menu is open

## Database changes
- No database schema changes
- Application settings gain sidebar grouping, order, and collapsed-section fields; installations saved before this release load them at their defaults
- Preserve existing Projects, Workspaces, terminals, Missions, Memory, settings, and Stable updater state

## Known issues
- A Windows protected-process, driver, or component-store fault can force a restart independently of PARALITH and cannot be repaired from within the application
- Windows component-store and protected-file verification require an elevated Administrator console
- Open in default app remains restricted by the opener path policy; Reveal in file explorer is available
- GitHub App installation-token exchange and public webhook ingress require the separately deployed Corelith backend service
- Remote repository synchronization remains explicit-refresh only
- Commit history is read on demand for the selected repository or worktree; it does not refresh automatically as new commits land
- Sidebar grouping and order preferences saved by an earlier release migrate once on first launch; a second machine keeps its own until it launches this version

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `a9f621a4ecdee1945c0bf91fd866499c3d7d059dc73a7d5208f08d23f8b37d2b  PARALITH_0.4.8_x64_en-US.msi`
- `ce3a2dd96934d041a8baa4ef10623c7dedf98c67a7c571f5e495133bbcade2f3  PARALITH_0.4.8_x64_en-US.msi.sig`
- `87ca38d3cae1b82cb4a4712e085ff9f2cf38581d8a024bdb0fc7594b011ac721  PARALITH_0.4.8_x64-setup.exe`
- `7e74f59ef54977e70d52a1c1a031057226c3c33e6fdd498c0f1413e880173055  PARALITH_0.4.8_x64-setup.exe.sig`
