# Decisions and authority — Staff Department
Updated 2026-10-19. This file separates **explicit Max choices** from suggestions. Where detailed behavior is still being worked out, see OPEN_QUESTIONS.md.

## Explicitly chosen
- **KISS is paramount**, not negotiable stylistic advice; minimize process, cost, tokens and distractions.
- There will be **one universal Staff Director**, a replaceable on-demand Codex agent with Git-backed institutional memory; product decisions and command belong elsewhere.
- Use **independent Codex sessions/chats, not subagents**. Agent histories are archived on retirement and their chats removed from active Codex UI.
- Staff Director hires, releases and updates affected current agents' instructions. Hot updates for compatible changes; recreate on material incompatibility. Director itself must also be recreatable.
- Roles are templates that can have **optional per-project extensions**. Common baseline Playbook and role library live in Staff Department; project-specific instructions live inside their own repositories. Do not multiply incompatible copies of canonical truth.
- **Orca is renamed Lead**. CTO is the project executive, Lead coordinates workers; CTO and Consultant collapsed to **CTO**. No mandatory always-on Inspector or all-roles-on-every-task policy.
- CTO is the project-specific Max interface and quality/product-outcome steward; at start of a new task, present understanding, uncertainties, options and preliminary plan for Max to confirm before execution. CTO can suggest a direct worker instead of Lead for small tasks, pending Max approval.
- Every agent and CTO should persist recoverable working state in Git-backed files, **not rely on chat or context compression**. Full history may be archived separately from active contexts.
- QA must test the **actual intended capability and real human usability**; use stage-appropriate coverage and defer broad regression appropriately. Remove temporary testing artifacts at the end.
- Staff Department architect may use **`architect/`** folder autonomously as its working memory, without treating it as a parallel product truth. Changes elsewhere in repository require Max's explicit approval/delegated permission. User's non-response to a suggestion never signifies agreement.
- Architect is the custodian with Max of canonical design documentation; others may maintain it within delegated authority. The architect is **not** a Codex staff role for now; CTO does not need to coordinate with it. Connected GitHub is the reference source for code and project context, including private repositories.
- **No implementation or role prompt authoring yet** until Max explicitly concludes discussion and approves.

## Proposals not automatically approved
- Exact file naming beyond `architect/`; precise role-template schemas; state registry format.
- Cross-project CEO/GM layer; auto project bootstrap; scheduling mechanism; staff activity-report design.
- Detailed cutoffs for compaction/replacement; polling around 10 minutes is a stated preference but can be calibrated.
- Specific role-specific base model/reasoning settings, pending availability and real trials.

## Care with public repo
Staff Department GitHub repository is PUBLIC. Do not publish sensitive personal profile data, private chats, tokens, credentials, or private repository material. Keep human-collaboration guidance focused on work behavior and scoped audiences.
## Additional explicit decisions, 2026-10-19

- **Real benefit rule:** Every new rule, check, abstraction or mechanism must solve an actual problem or bring an identifiable improvement. Novelty, conventions and hypothetical future needs are insufficient reasons. KISS is the overriding design constraint.
- **Canonical Playbook:** keep **one** authoritative universal Playbook in Staff Department; role library here, optional project-specific role instructions in their respective project repositories. Public-repository privacy for the imported source Playbook must be resolved before publishing it.
- **Git completion:** local commits are useful intermediate checkpoints, but a **finished task must be committed and pushed to its remote repository**. Commit without push is not delivery. Do not silently infer authorization to merge into an integration/main branch.
- **Build order:** first align and author the necessary universal roles and instructions, then implement/test a minimal Staff Director for hire/update/release of independent Codex sessions. Design reusable project scaffolding/bootstrap **after** that, not before.
- The present discussion is being synchronized. The user has **not yet issued final authorization** to author role templates or implement the Director.
