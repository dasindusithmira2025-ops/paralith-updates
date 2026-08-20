# PARALITH Stable 0.4.14

Channel: stable
Date: 2026-08-14
Git commit: 9acbbe6852d1c809ee92fca0846fc2af35f788ea
Database schema: 36

## Highlights
- Paralith Vault: adds a generated, reviewable project-intelligence vault with Markdown notes for features, modules, commands, database objects, risks, operations, roadmap items, and repository snapshots
- Memory workspace: introduces the in-app Memory surface with overview, search, graph, timeline, review, inspector, context, activity, and editor views backed by real Tauri commands
- Context Fabric: adds the canonical memory, claim, evidence, relation, knowledge job, project-fact, candidate, timeline, handoff, capability, branch-merge, and code-index schema needed for provenance-backed project knowledge

## Fixes
- Quick Open and file watching now avoid generated Vault and build/cache directories while preserving explicit user files
- Swarm handoff and context compilation now have persistent knowledge handoff records instead of relying only on transient agent output
- Project filesystem models now carry richer file metadata for intelligence and memory workflows

## Database changes
- Schema v34 adds Context Fabric and knowledge-intelligence tables for memory quality, wikilinks, claims, relations, jobs, candidates, conflicts, handoffs, timelines, project facts, capabilities, branch merges, and code graph indexes
- Schema v35 preserves repository audit provenance against live Swarm tasks and removes retired Mission foreign-key coupling while retaining historical rows
- Schema v36 persists the exact compiled ContextPack delivered to each Swarm AgentRun while preserving historical context-pack rows
- Existing Projects, Workspaces, terminals, Missions, prior Memory rows, Database Studio data, Usage history, settings, and Stable updater state are preserved through forward migrations

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
- `be32bc3bc6a6314677e015ac3fbfb23d0d478959ba99c9238a4e561a33ae15f2  PARALITH_0.4.14_x64_en-US.msi`
- `3341149c2093643f8a38817b4731deb66bfdbb0d9b1189282bf7bbb4b93a613a  PARALITH_0.4.14_x64_en-US.msi.sig`
- `ea09f1eb7f02fd1f8a7adf89a42dc8b168e254342fd0f97930c02c7e6ae8055e  PARALITH_0.4.14_x64-setup.exe`
- `6d8a7f10f6de90c72effac9b22306ed37529bc35f75b9b37931ca06a96b935a4  PARALITH_0.4.14_x64-setup.exe.sig`
