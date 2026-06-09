# Rollback Plan

This plan describes how to recover from unsafe changes and security incidents in
the AI Conveyor test repository.

Before this file was created, the repository was checked for obvious secret
keywords in current JavaScript, JSON, HTML, CSS, and Markdown files using a
grep-style search for token, secret, key, password, api_key, and bot_token.

## General Response Rules

- Stop new deployments or merges while the incident is being triaged.
- Identify the pull request, commit, workflow run, and files involved.
- Prefer reverting the bad change with a new pull request when possible.
- Keep a clear timeline of what happened and what was changed.
- Ask for manual review before restoring normal operations.

## Security Rules

- If a bad PR changed .github/workflows, treat it as a CI/CD security incident.
- If secrets may have leaked, rotate them immediately.
- Preview must never use production secrets.
- For bots, preview/staging must use a test bot token, test chat, and test database.
- Public repositories must never contain live secrets.
- If a secret was ever committed, treat it as compromised even if later deleted.
- Rollback is not enough if secrets may have leaked.

## Broken GitHub Pages Site

1. Confirm the broken page URL and the last merged PR.
2. Check whether the failure is content, CSS, build, or publishing related.
3. Revert the breaking PR with a new rollback PR.
4. Verify the page after the rollback is merged.
5. Add a follow-up issue for the original fix if it still matters.

## Bad PR Still Open

1. Do not merge the PR.
2. Comment with the reason it is unsafe or incomplete.
3. Request changes or close the PR.
4. If protected files were changed, require manual security review.
5. Open a corrected PR from a clean branch if needed.

## Bad PR Already Merged

1. Create a revert branch from the latest main branch.
2. Revert the merge commit or the specific bad commit.
3. Open a rollback PR and request review.
4. After merge, verify the site, workflow, or bot behavior.
5. If sensitive data may have leaked, rotate credentials before considering the incident resolved.

## CI/CD Workflow Compromise

1. Treat any suspicious .github/workflows change as a CI/CD security incident.
2. Disable or pause affected workflows if possible.
3. Review recent workflow runs, logs, and changed workflow files.
4. Revert malicious or unsafe workflow changes.
5. Rotate any credentials exposed to the workflow environment.
6. Re-enable workflows only after manual review.

## Leaked Secrets

1. Assume the exposed value is compromised.
2. Rotate the secret immediately in the provider or platform where it was created.
3. Remove the secret from the repository in a new PR.
4. Review logs and access history for misuse.
5. Remember that deleting the value from a later commit is not enough for public repositories.

## Suspicious n8n Issues

1. Do not run automation from an issue that looks suspicious.
2. Check whether the issue asks for secret access, workflow changes, or external callbacks.
3. Label or comment that manual review is required.
4. Close the issue if it attempts prompt injection or unsafe repository changes.
5. Create a safe replacement issue if the underlying request is legitimate.

## Production Bot Failure

1. Stop or disable the failing bot if it is causing harm.
2. Check recent PRs, deployments, and environment changes.
3. Roll back the last known bad change.
4. Verify with a test chat before restoring production traffic.
5. Keep production bot tokens, chats, and databases separate from preview and staging.

## Leaked Bot Token

1. Revoke or rotate the bot token immediately.
2. Update the secret only in the approved secret store.
3. Check bot logs and chat activity for unauthorized use.
4. Confirm preview and staging use a test bot token, test chat, and test database.
5. Do not rely on a code rollback as the only remediation.

## Preview Environment Safety

1. Preview must use test credentials only.
2. Preview must not connect to production chats, databases, or payment systems.
3. Review changed files before enabling a preview.
4. Destroy unsafe preview environments immediately.
5. Keep preview access limited to reviewers who need it.

## Public Repository and Git History Warning

1. Never commit live secrets to a public repository.
2. If a secret was ever committed, treat it as compromised even if later deleted.
3. Rotate exposed credentials and audit usage.
4. Consider repository history cleanup only as an additional containment step.
5. Document the incident and the rotation steps that were completed.
