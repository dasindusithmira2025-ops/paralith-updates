# PARALITH Stable 0.4.15

Channel: stable
Date: 2026-08-22
Git commit: f3b5ce5d7123aa6f5a4060dc1a716bca69b5ec72
Database schema: 37

## Highlights
- Swarm creation now preserves canonical provider and model identities for built-in presets, duplicated presets, custom presets, and review snapshots
- Built-in Swarm presets are repaired during schema migration when older databases stored concrete agent allocations without model configuration
- Stable release metadata now matches runtime schema 37 so the protected release workflow can validate the tagged build

## Fixes
- Built-in Swarm teams no longer appear complete while carrying `Model not configured` members that cannot launch
- Provider and model changes in the Swarm roster are committed to the launch request instead of falling back to stale or missing identities
- Unavailable or retired models are reported as unavailable by canonical id, while unauthenticated providers remain distinguishable from missing model configuration

## Database changes
- Schema v37 refreshes built-in Swarm presets so concrete agent allocations carry canonical provider and model identities
- User-created Swarm presets, Projects, Workspaces, terminals, Missions, Memory rows, Database Studio data, Usage history, settings, and Stable updater state are preserved through forward migrations

## Known issues
- The Vault Markdown directory is a generated review surface; the runtime SQLite database remains the canonical source for in-app memory and evidence
- Editing generated Vault notes outside PARALITH does not yet import changes back into the runtime database
- Knowledge extraction and candidate promotion remain deterministic workflow surfaces; agent-generated claims still require evidence and review before they become verified memory
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
- `5f49a3480fe1f7926a67464d0a3162e10953c7abadc1306a39d83d97c319c62c  PARALITH_0.4.15_x64_en-US.msi`
- `28359c18fe3877900fbcf64269f72df26acab5dacdaffae532d797531fc8601f  PARALITH_0.4.15_x64_en-US.msi.sig`
- `029fe2fc8a1eb720058d422907e9c3a23b68909ac4fe9650a1ec554143b6757f  PARALITH_0.4.15_x64-setup.exe`
- `c7c9da43fed347acf7b596491a54c106d72f44263cc236ae057329d0f3745e46  PARALITH_0.4.15_x64-setup.exe.sig`
