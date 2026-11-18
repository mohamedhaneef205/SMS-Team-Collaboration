# Security and privacy

This application handles school data, credentials, and role-based access. Treat the repository as sensitive even when it is private.

- **Never commit:** MySQL passwords, bootstrap secrets, JWT/session/cookie values, service tokens, real student data, parent contact details, uploaded assignments, database dumps, or full IntelliJ/.git/target folders.
- Read values from environment variables and use dummy values for screenshots/tests.
- Review changes and imported ZIP contents before publishing.
- If a password was already committed, rotate it. Deleting a line from the latest commit is **not sufficient** to remove historical exposure.
- Never paste real secrets in GitHub Issues, PRs, or commit messages.
- Check authorization on the backend, not only by hiding frontend buttons.
- Security findings should be reported privately to the repository maintainer, not disclosed with exploit details in public Issues.

The repository owner should verify visibility under GitHub Settings → General → Danger Zone → Change repository visibility. This connected workflow cannot change that setting automatically.
