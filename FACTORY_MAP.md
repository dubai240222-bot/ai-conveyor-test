# AI Conveyor Factory Map

## Current Repository

- Repository: `dubai240222-bot/ai-conveyor-test`
- GitHub Pages URL: `https://dubai240222-bot.github.io/ai-conveyor-test/`
- GitHub Pages deploys from main/root.
- Branch Protection protects `main`.
- Merge to `main` is manual.

## Current Conveyor

The production n8n form creates GitHub Issues automatically. Those Issues are
the task queue for the factory.

Codex is currently manual, not automatic. A human starts Codex, points it at an
Issue, reviews the proposed change, and opens or reviews the resulting Pull
Request.

## Safety and Review

- GitHub Actions protected-files-check works and checks Pull Requests for protected file changes.
- RawGitHack preview is temporary/manual and should only be used for review before merge.
- Secrets must never be stored in the public repository.
- Sensitive configuration must live outside the public repo, such as in GitHub Secrets or private local environment files.

## Flow

```text
n8n production form
  -> GitHub Issue
  -> manual Codex session
  -> Pull Request
  -> protected-files-check
  -> manual preview review
  -> manual merge
  -> GitHub Pages deploy from main/root
```
