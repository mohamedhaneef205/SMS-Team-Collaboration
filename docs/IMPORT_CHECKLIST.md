# Import checklist — uploaded application source

This repository initially contained only a README. Team workflow files can be added here, but the actual Java project must be imported as separately reviewable source files.

## Before importing

- [ ] Repository owner has checked whether public/private visibility is appropriate.
- [ ] Rotate any MySQL password already published or shared.
- [ ] Start from a clean extraction of the supplied project ZIP.
- [ ] Exclude `.git/`, `.idea/`, `target/`, archives, exports, uploads and other generated files.
- [ ] Replace literal MySQL credentials in `application.properties` with environment variable placeholders.
- [ ] Exclude or manually sanitize `sql.sql`: uploaded copy mixes DDL with INSERT/UPDATE/DELETE statements.
- [ ] Review sample HTTP requests and all source comments for secrets or student personal data.
- [ ] Preserve original Java class and package names.
- [ ] Compile locally and compare frontend endpoints with Spring Security rules.

## Import the source

1. Clone this new repository locally.
2. Copy **only vetted source directories** (`src/main/java`, `src/main/resources`, `src/test`, `.mvn`) and Maven wrapper/POM into the cloned repository.
3. Run `git status`, `git diff --cached`, and an additional secret scan before committing.
4. Commit as a clean baseline authored by the actual person importing the preexisting project.
5. Push the baseline to `main`.
6. After baseline import, each teammate should update their branch from `main` before writing new code.

**Do not misrepresent the baseline import as newly written work by each member.**

## Verified vs pending

- GitHub collaboration infrastructure: tracked in this repository.
- Complete application source import: pending until source files appear here.
- Compilation/test results on this repository: pending.
- Member GitHub username assignment: pending confirmation.
