# Issue to Codex Handoff

This checklist describes the manual procedure for safely moving a GitHub Issue
into a Codex implementation session.

## 1. Required Issue Fields Before Starting Codex

- Clear task
- Repository name
- Do-not-touch files
- Acceptance criteria
- Risk notes if needed

## 2. Safe Labels

- `ready-for-codex`
- `needs-review`
- `unsafe-request`
- `ai-generated`

## 3. Operator Checklist Before Starting Codex

- Check issue title
- Check acceptance criteria
- Check protected files
- Confirm no secrets are included
- Copy the Codex handoff command from the Issue body
- Start Codex only after these checks

## 4. Codex Safety Rules

- Create a new branch
- Do not change unrelated files
- Do not touch protected files
- Open a Pull Request
- List changed files in PR
- Mention the Issue in PR

## 5. After PR Is Opened

- Check Files changed
- Check protected-files-check
- Check no conflicts
- Preview only if site files changed
- Merge only after checks are green
