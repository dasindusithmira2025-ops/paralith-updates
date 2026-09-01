# PARALITH Stable 0.4.18

Channel: stable
Date: 2026-09-01
Git commit: 176d0d24fccdeced79213ac3a53a6aba7bd036e9
Database schema: 40

## Highlights
- Paralith Brain provides one project-scoped intelligence contract for asking questions, retrieving evidence, exploring systems, and inspecting the exact context received by an agent run
- Brain answers are deterministic and evidence-backed: sources, related knowledge, history, confidence, staleness, and the number of considered records remain visible instead of being presented as generated certainty
- Memory is now presented as Brain across the project surface, with focused Ask, Explore, Activity, Decisions, Review, and Search workflows
- Workspace surfaces share a consistent Files, Editor, Browser, and terminal-pane interaction model with progressive disclosure for secondary actions

## Fixes
- Brain reads and proposals are project-scoped through the existing Context Fabric boundary, while external-style proposals enter the candidate funnel instead of writing canonical truth directly
- Brain retains provenance for sources, related items, timeline history, and immutable per-run context so an answer can be inspected and challenged
- File Explorer groups dot and system directories behind an explicit disclosure row without removing access to them
- Editor and Browser chrome use the same compact surface hierarchy, and empty editor state offers Quick Open plus real recently opened files

## Database changes
- No schema change: the existing Context Fabric, memory, evidence, timeline, and agent-run context records are reused and existing user data is preserved

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
- `4a604f343fd58148dbb3b3db1fe89f7269eb88186c2810c16687a8b85e28bc8e  PARALITH_0.4.18_x64_en-US.msi`
- `080c57df90ca91c8dc9cc5b2a3870d814261077263608236083c2c9f9cecbe69  PARALITH_0.4.18_x64_en-US.msi.sig`
- `8ec9f09d2578a78a09e6ccddbd64c29d206c6c016842e94ad26dc29aeb539f1a  PARALITH_0.4.18_x64-setup.exe`
- `2fdfb6e4d9da91159abf97483eb16b4e54374fb12dc5091d46d3345fce7da32d  PARALITH_0.4.18_x64-setup.exe.sig`
