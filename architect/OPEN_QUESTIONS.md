# Open and deferred questions — Staff Department
Updated 2026-10-19. **Not a task queue or implementation mandate.** These ideas were discussed but not finally specified.

1. **Agent context life**: How long reuse healthy existing sessions? What signals identify deteriorating context before compaction, and when to fresh-start vs hot-update? Do not impose arbitrary churn.
2. **Instruction versioning / propagation**: Trigger from Git changes or manual request? Which project overlays count? How to update busy threads without disrupting useful work; how to confirm adoption. Keep minimum per-agent versions/IDs.
3. **Recoverable state schema**: Minimal portable current-work checkpoint for CTO, Lead and specialists; how to avoid redundant product truth, stale links or copying full chats.
4. **Director runtime / interface**: Exact invocation mechanism from independent Codex chats, registry format, archive format and safe session deletion; prove actual Codex APIs in a small prototype.
5. **Concurrency and ownership**: how many simultaneous Leads/teams/projects; shared worktree hygiene, scoped working directories, edits collision; who holds and releases a worker.
6. **Watchdog**: Simple shared scheduler ~10-minute provisional poll; which true progress signals and estimated time threshold prompt a CTO; what happens if CTO/Codex/host is offline; no automatic killing merely for slowness.
7. **Time estimation learning**: minimal estimate/actual/error history and how to calibrate over multiple tasks without elaborate analytics.
8. **Reports**: second-phase scripted query: who active, time worked, accomplished outcomes/failures today. Logs vs transcripts and storage policy. Director requested only; no permanent monitoring LLM.
9. **Project lifecycle**: bootstrap new private/public repo, canonical docs and role overlays without templated bureaucracy, and adopt existing projects without overwriting conventions; later than initial role/Director design.
10. **Possible General Manager/CEO**: overarching multiple-project view (distinct from Staff Director). Concept parked.
11. **CTO role self-review**: avoid CTO protecting its own mistakes; decide when a fresh independent Inspector is valuable vs needlessly procedural.
12. **Roles**: confirm initial full role catalog and names, particularly Concept Artist vs Visual Designer/Art Agent, Inspector, UX vs Usability QA vs Visual QA, DevOps vs Release Engineer, technical QA, Worker, Documentation Steward, Investigator, Researcher. No arbitrary seven-role cap.
13. **Architect persistence UX**: short user custom-instructions block to trigger architect mode for any repo; incremental write points without delaying each quick conversation. Draft after approval.
14. **Future external interfaces**: Telegram CLI bot for notification/escalation, Dot, custom local UI. Deliberately deferred.
15. **Review/QA**: decide when focused QA or no QA is appropriate and when separate pre-release regression is justified, without mandatory universal gates.
16. **Authority and security exceptions**: apply low-ceremony trust defaults but explicitly determine real risk boundaries for public users, payments, valuable data and credential exposure case by case, not generic theatre.
17. **Architect's canonical-document edit authority:** autonomy is currently scoped to `architect/`, while canonical specs may live elsewhere. Should the architect have standing write permission to update *already approved* project truth outside `architect/`, or seek permission each time? No implicit expansion.
18. **Public Staff repository and Playbook privacy:** the source Playbook includes personal collaboration context. Decide whether to make Staff private or publish an appropriately scoped public-safe canonical Playbook; do not upload sensitive details by default.
19. **Work history archive location:** work state stays portable in each project's Git; raw agent transcripts can be large and sensitive. Choose archive location/retention at pilot time, without dumping everything into the public Staff repo or new agent prompts.
20. **Finished task boundary:** distinguish completed/accepted deliveries from partial progress and diagnostic failures. Final deliverables require commit and remote push, but no automatically authorized merge.
