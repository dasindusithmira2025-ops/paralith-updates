# PARALITH Stable 0.4.20

Channel: stable
Date: 2026-09-02
Git commit: 58dde0e3cacc1179c8b95ed0985170f98f6cf2ba
Database schema: 41

## Highlights
- Source Control now includes an interactive commit Graph that makes repository topology visible as compact lanes, including merge commits and continuing parent relationships across loaded history pages
- Graph selection keeps the real commit inspector available and shows active-worktree changes from the repository snapshot alongside the commit history

## Fixes
- None

## Database changes
- No database schema changes; the graph uses the existing bounded repository history and commit-detail services

## Known issues
- The graph intentionally does not claim commit-level task, agent, proof, or GitHub provenance because existing persistence does not establish those associations reliably
- Worktree management and advanced Git operations remain separate workflows

## Required manual actions
- Use the in-app Stable update button and approve the safe restart; no manual installer download is required

## SHA-256
- `3db7079adf8637ba8239de8d750f2b805aa3d2c30dd43e2d9968b0bfef0e912f  PARALITH_0.4.20_x64_en-US.msi`
- `29a50a91f008f795cdd4f5adcda8eed4ee34806b82984ca60f68a7ae8b95c707  PARALITH_0.4.20_x64_en-US.msi.sig`
- `64c1b8698b13245ff2e1e97fdbe2f3f8fc2fcf8701bc2eb86acff54e574595a2  PARALITH_0.4.20_x64-setup.exe`
- `8f73cc2903d227c1fbe76bef4c2f10887f02f5dc06e33de7caf1607a58a4e946  PARALITH_0.4.20_x64-setup.exe.sig`
