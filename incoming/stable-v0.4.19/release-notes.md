# PARALITH Stable 0.4.19

Channel: stable
Date: 2026-09-02
Git commit: 79c40ec411588e2919d699b9da797e7310b0fd1e
Database schema: 41

## Highlights
- Activity provides one live view of agent runs and GitHub workflow runs, grouped by work that needs attention, work still running, and recent outcomes
- Important agent and workflow transitions now appear as focused in-app alerts and, while Paralith is in the background, native operating-system notifications
- Protected GitHub deployment reviews can be approved or rejected from Activity only when the signed-in account has GitHub's required environment permission

## Fixes
- Agent usage limits, authentication requirements, permission requests, cancellations, and unexpected exits are presented as distinct outcomes instead of one generic failure
- Activity survives application restart, ignores stale or duplicate provider updates, and permanently removes settled items that the user dismisses
- Consecutive agent runs in the same workspace pane retain separate identities so a completed run cannot hide the next one
- Activity hydration preserves newer realtime transitions that arrive while the initial persisted snapshot is loading

## Database changes
- Schema 41 adds the activity_threads table and bounded indexes for unresolved work and recent outcomes; existing project, workspace, terminal, Memory, and Usage data is preserved
- The normal pre-migration backup runs before upgrading an existing database

## Known issues
- GitHub workflow activity requires an authenticated GitHub CLI session and a repository GitHub can identify; agent activity remains available without GitHub
- Native notifications require operating-system permission; the in-app Activity pulse and alerts remain available when permission is declined
- Usage cost is an equivalent API list-price estimate, not a provider subscription bill; models without a known rate keep their tokens visible and make the total partial
- The Source Control commit Graph remains outside this release

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required
- Allow notifications when prompted if background operating-system alerts are wanted

## SHA-256
- `d038db718f6fe7d816a7b72e60e61f4940421ae39ba6208efd7e50ccba8ad884  PARALITH_0.4.19_x64_en-US.msi`
- `598d78838cd608b0ebf368ee8e882b1b8fcf1cadde23ed2c1a4a64d364443736  PARALITH_0.4.19_x64_en-US.msi.sig`
- `0b8ef2bec5f80e1d9e8485e11035760eb14861d543d4d1f34abb5ec0c59cfcab  PARALITH_0.4.19_x64-setup.exe`
- `226ccb502e174e3dfb72e2db5563f27a35bd0af2e6b8fb7b47b6d1d1e51ad758  PARALITH_0.4.19_x64-setup.exe.sig`
