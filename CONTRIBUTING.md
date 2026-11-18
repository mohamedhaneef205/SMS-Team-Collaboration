# Contributing to the School Management System

## Agreement

1. Each member uses their **own GitHub identity**. No shared accounts or fabricated attribution.
2. Keep `main` suitable for demonstrations. Work on a branch for every task.
3. **Never replace or rename existing Java classes without agreement and a migration plan.** Coordinate schema changes and API contracts.
4. Do not upload personal data, SQL dumps of school records, secrets, IDE metadata or `target/`.
5. Link your PR to the corresponding issue; document what changed and how you tested it.
6. A different member should review every PR. No self-approval.
7. Changes enter `main` only after successful review and compilation/testing; incomplete work stays in its branch.

## Workflow

- Pick an unassigned issue, agree on scope, and add your GitHub handle as assignee.
- `git switch main`, then `git pull origin main`.
- `git switch -c feature/<short-task-name>` (or `fix/<short-task-name>`).
- Make small commits with descriptive messages such as `feat(student): validate profile lookup`.
- Run `.\mvnw.cmd -DskipTests compile` on Windows; run available relevant tests where safe.
- Push the branch: `git push -u origin feature/<short-task-name>`.
- Open a pull request into `main` and complete the PR checklist.
- Reviewer checks functionality, access control, data validation, tests, privacy and backwards compatibility.
- After review, merge using the normal GitHub PR interface and update local `main`.

## Recommended review checklist

- [ ] Existing class names and entity mappings remain compatible.
- [ ] Admin-only actions cannot be performed by teachers.
- [ ] Teacher scopes restrict grade and subject data appropriately.
- [ ] No hardcoded credentials or sensitive student data.
- [ ] SQL changes are documented and safe for existing databases.
- [ ] New/changed behavior has tests or reproducible manual test steps.
- [ ] UI calls the correct endpoints and handles errors.
- [ ] Build passes; merge conflicts resolved.
- [ ] PR description explains the member's own work accurately.

## Collaboration conventions

Use GitHub Issues for requirements/bugs, PRs for review, and GitHub Projects (To do / In progress / In review / Done) to track progress. Keep module work in short-lived branches. After an issue merges, create a new branch from the newest `main` for the next change.

## University viva

Each member should be able to show their issue, code diff, tests, PR discussion and explain their implementation. Do not recreate earlier work merely to generate misleading contribution statistics.
