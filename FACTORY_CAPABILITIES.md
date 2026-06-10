# AI Conveyor Factory Capabilities

## What the Factory Can Do Now

- Accept requests through the n8n production form.
- Create GitHub Issues from form submissions.
- Use Codex manually to turn Issues into repository changes.
- Open Pull Requests for review.
- Run the GitHub Actions `protected-files-check` on Pull Requests.
- Deploy the site with GitHub Pages from `main` and the repository root.
- Use manual RawGitHack previews for temporary branch review.
- Protect `main` with Branch Protection and manual merge review.

## What It Can Do with Small Setup

- Add a label-based handoff from GitHub Issues to the next manual Codex step.
- Add automatic Pull Request comments with preview links.
- Add reviewer assignment rules for factory PRs.
- Add a lightweight preview checklist to each PR.
- Add simple content or link checks before merge.

## What It Cannot Do Yet

- Start Codex automatically from a new Issue without a human.
- Fully automate preview review.
- Automatically merge approved Pull Requests.
- Guarantee rollback without human review.
- Use production secrets in previews or public repository files.

## Next Recommended Workshop

Add an Issue-to-Codex workshop that reduces the manual handoff after n8n creates
a GitHub Issue. The workshop should define labels, required Issue fields,
operator steps, and a checklist for starting Codex safely.
