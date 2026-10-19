# Current design context — Staff Department
Updated 2026-10-19. **Discussion baseline; no permission yet to implement.**

## North star
Build genuinely useful products, not satisfy tasks/checklists. KISS is a **binding governing constraint**, not a suggestion. Every step, test, report, safety layer, abstraction and token expenditure needs an actual purpose. Do not build a corporation, process gates, or generic frameworks. Trust Max and known collaborators. Security/compatibility hardening beyond real demonstrated needs requires explicit Max approval. Before a public release, replace obsolete implementation cleanly rather than carry old compatibility baggage without an actual consumer.

## Organization
- **Staff Director**: one replaceable on-demand Codex agent with its own Git-backed role library. Not a general manager, CTO, scheduler of product work, or permanent thinking LLM. Provides independent Codex chats/sessions (NOT subagents), selecting role, model, reasoning and the right assembled instructions. Requested CTO by Max; workers by Lead; team Lead requested by CTO. Max can explicitly request any specialist for any project.
- **CTO**: one logical position per project; session may be replaced. Receives a high-level assignment; first explains understanding, material questions, alternatives and an initial plan to Max for alignment. With approval, decomposes and assigns work, ideally to a Lead/team; for trivial tasks can suggest skipping Lead/team, with Max approving that exception. Protects actual product, reviews meaningful diffs and results, accepts/rejects, reasons about failures and interventions, calibrates time expectations and proactively reaches Max only when a real decision is needed. CTO has no obligation to know or contact a ChatGPT architect.
- **Lead** (formerly Orca): coordinates one team/task package, passes tasks to workers and QA, handles correction loops and progress; reports key events/blockers to CTO, not every detail. Teams may work in parallel by Max's decision.
- **Specialists**: selected per task, never obligatorily deployed all at once. Builder implements within instructions and approved scope; QA verifies relevant risk and actual user outcomes; Worker handles mechanical chores; UX / creative concept artist / other experts are available on demand. A role is a repeatable template; an agent is an independently addressable session with an ID.
- **Architect (ChatGPT conversation)**: Max invokes this role when needed. It is separate from the Codex staff hierarchy. Architect is co-owner with Max of canonical design truth, maintains design conversation context, documents nuanced decisions, reasons, tradeoffs and revisions. CTO can update factual implementation/project records as delegated. ChatGPT may read private GitHub repos through the connected integration. No mandatory ChatGPT Project uploads or CTO→architect communications.

## Director duties (v0 aim)
Hire: select model/reasoning; combine universal collaboration principles + role + project overlay + exact request. Return agent ID to requesting agent. If a project needs an instruction folder and lacks one, create project-scoped templates only for roles actually used, without overwriting existing project truth.
Release: archive sufficient work/session transcript, timing, outcome and necessary context, then remove session from Codex app so chats do not pile up. Do not force an LLM to compose long evidence bundles. Keep agent's **current recoverable work state** in project repo while active; archived history is for retrospective diagnosis, not prompt context.
Refresh: on changes to common/role/project instructions, find affected live agents; deliver small compatible updates in-place, or replace incompatible agent after preserving state. Director itself must be recreatable from its repository and docs.
Future: scripted staff/activity reporting on request, minimal registry, and cross-project watchdog integration. Never turn Director into product manager.

## Project state and agent recovery
- Git repo is canonical and portable; chat memory and compression cannot be trusted for continuity.
- Separate product truth (specs/decisions/architecture) from agent working state (task queue, assignment, open issues, current next actions, runtime identity, estimates, workspaces). Provide standardized but light project locations. Respect existing conventions rather than duplicating docs.
- Agents may keep their context within the same productive assignment; fresh sessions when context degrades, role changes materially, or task ends. After release retain an archive, not the whole transcript in new workers' context.
- Avoid uncontrolled extra checkouts/worktrees; clean all temporary QA artifacts/clones after use.
- Important problems, failed approaches, corrections from Max and process lessons should be recorded to avoid repeating mistakes, but not promoted automatically to permanent universal rules.

## Time and outcomes
- CTO estimates approximate elapsed time when task is assigned and revisits accuracy against results. Usually work lasting >~1 hour is a signal to inspect decomposition, not an unconditional deadline; some tasks naturally take longer.
- A simple shared watchdog may poll roughly every **10 minutes** (provisional preference), compare actual progress to estimates and nudge an active CTO for a meaningful delay. CTO investigates Lead or work directly; never auto-kill solely because of timer.
- Keep small machine-readable or plain-text records: task ID, agent ID, project, role, model/reasoning, start/end, estimate vs actual, outcome, key events and references to archived logs. Use existing Codex events where possible, no verbose manually-written evidence.
- An unsuccessful technical attempt is an outcome to record; the *goal* still governs whether work is complete. Iterate intelligently; avoid polishing proof of failure instead of solving.

## Quality / execution
- CTO gives each role the right **task granularity**: requirements specific to this work, not repetitive copies of permanent role instructions.
- Builder should know how to implement and avoid product-level invention; low/unnecessary reasoning can cause scope creep as much as underthinking can cause mistakes.
- QA is scoped to the current stage and risk. Focused testing now; broader regression/pre-release testing when integrated product is ready. Never test every hypothetical corner case merely because it can be imagined.
- Usability QA: actually try controls with mouse/touch, discover actions, check what happens and whether it serves a **human's** goal; not just a handler, DOM, accessibility score, or generic UI convention. Audience varies: Max alone, a handful of known people or public users.
- Inspector/Reviewer is a **fresh, conditional independent reviewer**, including goal alignment and the product experience, not an automatic gate; CTO owns daily continuity and acceptance.
- Visual concept/creative role first investigates brief, references, styles and suitability; draws only when direction is understood. Distinct from production art.
- Worker/Service Operator does precise packaging/moves/copying/cleanup without redesign, audits, unsolicited checks or sprawling evidence.
- OOP, generic wrappers, safety rails, backwards compatibility, processes and security overengineering are not defaults. Ask Max before significant systemic additions.

## Models and external interfaces
Model/reasoning are role- and problem-dependent; Max has preferred GPT-5.6 Sol for Codex, avoids GPT-6.x for execution based on observed behavior. CTO may selectively escalate reasoning/change agent based on a cause, not blindly.
Telegram notification bridge, Dot, generic CEO/GM hierarchy, project boilerplate/bootstrap and rich staff analytics are **deferred questions**, not implemented requirements.
Architect prefers fast conversational exchange; deep/pro reasoning reserved for major design, tasks and final review. Meaningful knowledge capture, not a Git write after every conversational reply.
