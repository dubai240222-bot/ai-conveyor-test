# Factory Journal

This journal records key milestones and decisions for the AI Conveyor project.
Future engineers: read `FACTORY_OPERATING_MANUAL.md` first, then continue from
the current status here.

## Current Status

- Mini Factory v0.1 is operational for simple static website tasks.
- n8n form creates GitHub Issues.
- New Issues include a Codex handoff command.
- Codex is still started manually.
- PR review and merge are still manual.
- `protected-files-check` works.
- GitHub Pages publishes from main/root.
- Homepage includes a modern STC 5G eSIM promo section.
- Existing AI Conveyor content remained visible after product work.

## Completed Milestones

### Factory Documentation Created

- `FACTORY_MAP.md` was created to describe the factory layout and component roles.
- `FACTORY_CAPABILITIES.md` was created to describe current and near-term capabilities.
- `FACTORY_JOURNAL.md` was created to preserve milestone and shift history.

### Codex Handoff Improved

- New GitHub Issues include a Codex handoff command.
- `ISSUE_TO_CODEX_HANDOFF.md` was added to standardize manual Issue-to-Codex handoff.

### First Product Test Released

- PR #31 was merged.
- The homepage now includes a modern STC 5G eSIM promo section.
- GitHub Pages updated successfully after merge.
- Mini Factory v0.1 can handle simple static website tasks.

### Factory Operating Manual Added

- `FACTORY_OPERATING_MANUAL.md` was added as the mandatory first-read document.
- Future shifts should follow its reading order, shift start protocol, engineer rules, and handover template.

## Active / Manual Parts

| Component | Current v0.1 status |
| --- | --- |
| n8n form creates GitHub Issues | Automated |
| Issues include Codex handoff command | Present in new Issues |
| Codex start | Manual |
| PR review | Manual |
| PR merge | Manual |
| protected-files-check | Works |
| GitHub Pages publishing | Publishes from main/root |

## Locked Decisions

- Do not build auto-Codex without owner approval.
- Do not build auto-merge without owner approval.
- Do not add databases, payments, or complex deployment without owner approval.
- Do not change protected files or secret paths without explicit owner approval.
- Keep `ROLLBACK_PLAN.md` and `.github/workflows/protected-files-check.yml` intact unless the owner explicitly asks to change them.

## Next Safe Step

- Continue product work or improve the eSIM-first homepage only after confirming latest status.
- Do not build auto-Codex, auto-merge, databases, payments, or complex deployment without owner approval.
- Start every future shift by reading `FACTORY_OPERATING_MANUAL.md` and this journal.
