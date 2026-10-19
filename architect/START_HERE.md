# Architect workspace — START HERE

Project: **Codex Staff Department**. Status: **design discussion; implementation not yet authorized**.
Last synchronized: 2026-10-19.

This folder is the working memory of the project architect, not a competing source of project truth. The architect can be a new ChatGPT conversation: the role persists in files, not in chat history.

## First steps for a new architect
1. Read this file, `CONTEXT.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md`.
2. Read canonical specifications / playbook / roles when they are added to the repository; link to them here rather than copy them.
3. Read the actual Git branch and implementation before claiming the system exists or works.
4. Distinguish **user-approved decisions**, **architect suggestions**, and **open questions**. User silence is not approval.
5. Keep working context accurate after *meaningful* conversations and decisions. Do not run a writing/commit ceremony after every message.

## Authority and write boundary
- Max makes final product/organizational decisions; architect maintains design context and consistency of project documentation. CTO/others may maintain documentation only under delegated authority.
- Architect may maintain files **inside `architect/` autonomously**. Outside it, writes require Max's express permission or a clearly delegated scope.
- One fact/decision has one canonical home. Never maintain a second conflicting copy in `architect/`.
- Current notes record the discussion; they do **not** authorize producing role prompts, executable code, or a working Director before Max approves.
- This repository is **PUBLIC**: do not publish raw chat histories, personal data, credentials, private project code, or unreviewed confidential artifacts here.

## Purpose
A simple reusable staff service for independent Codex agent sessions, role instructions and project-specific overlays. Priority: KISS; real product outcomes; minimum process, attention and token expense.

See `CONTEXT.md` for the current design picture; `DECISIONS.md` for explicit approvals; `OPEN_QUESTIONS.md` for unresolved and deferred matters.
