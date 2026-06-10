# Factory Operating Manual

Mandatory first-read document for every future AI engineer shift.

## Core Mission

This project is not rebuilding Lovable or Bolt.

It is a small personal AI workflow for a non-programmer. The goal is to help one
person ship small digital products with less manual copying between tools.

Do not treat the factory as a platform, startup architecture, or abstract
engineering playground. Keep it practical, small, and understandable.

## Mandatory Reading Order

Before changing anything, read these files in order:

1. `FACTORY_OPERATING_MANUAL.md`
2. `FACTORY_MAP.md`
3. `FACTORY_CAPABILITIES.md`
4. `FACTORY_JOURNAL.md`
5. `ISSUE_TO_CODEX_HANDOFF.md`
6. `ROLLBACK_PLAN.md`

Do not skip context. Do not assume previous shifts already explained the current
state well enough.

## Shift Start Protocol

At the start of every shift:

1. Read the mandatory files in order.
2. Find the latest `FACTORY_JOURNAL.md` entry.
3. Check the current GitHub Issue and any linked Pull Request.
4. Confirm protected files and do-not-touch files before editing.
5. Report only the current status, last completed step, and next safe step.

Keep the shift-start report short. The user needs orientation, not a full system
lecture.

## Engineer Rules

- Work from the GitHub Issue that the user identifies as source of truth.
- Create a new branch for each task.
- Keep changes scoped to the files allowed by the Issue.
- Do not redesign the factory without explicit written permission.
- Do not add new tools when the current workflow can solve the task.
- Do not jump ahead to auto-Codex, auto-merge, payments, databases, or complex deployments without approval.
- Do not make the user act as a technical courier across many tools.
- Prefer clear replacement instructions when editing n8n code nodes.
- Finish the current task before proposing the next one.
- If the next step is unclear, ask one short question.
- Never add secrets, tokens, API keys, private keys, bot tokens, or credentials.

## Mini Factory v0.1 Definition

Mini Factory v0.1 is the approved current workflow:

```text
n8n form
  -> creates GitHub Issue
  -> Issue contains Codex handoff command
  -> user starts Codex manually
  -> Codex opens Pull Request
  -> protected-files-check runs automatically
  -> user reviews preview manually when needed
  -> user merges manually
  -> GitHub Pages publishes from main
```

This version is intentionally simple. It is suitable for simple static website
tasks and documentation tasks. It is not a fully automatic software factory.

## Strict Shift Handover Journal Template

Every meaningful shift should end by adding or preparing a journal entry in this
format:

```markdown
## YYYY-MM-DD

- Completed:
- Working:
- Manual:
- Blocked:
- Next target:
- Files changed:
- Pull Request:
```

Rules for journal entries:

- Keep entries factual and short.
- Mention merged PR numbers when relevant.
- Record tests separately from product changes.
- Record whether protected files were touched.
- End with one clear next target.
