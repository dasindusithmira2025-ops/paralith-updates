# PARALITH Stable 0.4.13

Channel: stable
Date: 2026-08-13
Git commit: 9b5215def1a448ffe279c58ae6796e13245b5ef8
Database schema: 30

## Highlights
- Usage analytics: PARALITH now persists daily AI token history by provider and model, with local 7/30/90-day views, provider/model/day breakdowns, cache-read savings, and partial-cost labeling when a model has no known list price
- Workspace surface: the workspace tool panel now uses explicit surface tabs and empty states so Browser, Usage, and other tools have clear ownership instead of competing panel state
- Sidebar: the workspace sidebar has been reorganized into a focused header, workspace section, scroll body, and status area, with update actions available from the persistent status region

## Fixes
- Codex usage parsing now reads token counters from the CLI's info envelope and carries the serving model across transcript events, so Codex history is no longer silently recorded as zero or model-less
- Codex cached input is normalized before aggregation so cached tokens are not counted twice as uncached input
- The update notification and sidebar update action now share the same actionable-phase logic and restart confirmation copy

## Database changes
- Schema v30 adds ai_usage_daily for bucketed provider/model/date token aggregates only; it stores no transcript text, prompts, session ids, or file paths
- Existing Projects, Workspaces, terminals, Missions, Memory, settings, Database Studio data, and Stable updater state are preserved

## Known issues
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
- `a3073432238dcde90772ac8a38d3ecdbbbdb35c93ca8558486891f28e205fedc  PARALITH_0.4.13_x64_en-US.msi`
- `15c95e01a2891f3ffec9e2c67862844f643e6684cc5f423d606a465bc4ce2ea6  PARALITH_0.4.13_x64_en-US.msi.sig`
- `227ddbd1edd5497b0beaf04d5de2fe4280cebfb70c6f2cc41e4892d958f96453  PARALITH_0.4.13_x64-setup.exe`
- `88e4732152722982c25548b9f62e2aa3cbd80c5c1fdfdfcc35ac957a3c8a3652  PARALITH_0.4.13_x64-setup.exe.sig`
