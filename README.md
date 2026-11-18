# School Management System — Team Collaboration

Java Spring Boot + MySQL + HTML/CSS/JavaScript | Six-member university project.

> **Repository setup status:** Team workflow and documentation are being prepared. The complete application source has not yet been pushed from the local IntelliJ project. Do not represent this repository as a tested deployment until the code is imported and verified.

## Overview

This project aims to manage school data through separate administrator and teacher workflows:
- Student registration, grades, and profiles.
- Teacher registration, accounts, grade/subject permission scopes.
- Attendance, subject marks, assignment marks, and teacher assignments.
- Grade 1, intermediate, Grade 6 scholarship, and A/L admissions.
- Physical properties and non-academic staff.
- Administrator/teacher authentication and role-based authorization.

The uploaded local source uses the package `SchoolManagementSystem`, Spring Boot 4.1.2, Java 23, Maven, and MySQL.

## Source layout (to be imported)

- `src/main/java/SchoolManagementSystem/` — application, entities, controllers, services, repositories, and security.
- `src/main/resources/static/` — frontend HTML/CSS/JS.
- `src/main/resources/application.properties` — configuration using environment variables, **without real passwords**.
- `src/test/` — automated tests and test notes.
- `pom.xml`, `mvnw`, `mvnw.cmd` — Maven build.
- `docs/` — architecture, team responsibilities, process, and setup.

## Local setup (once source is imported)

1. Install JDK 23, MySQL, Git and IntelliJ IDEA.
2. Create a local database named `school_management`; review any SQL schema before execution.
3. Set environment variables locally: `DB_URL`, `DB_USERNAME`, `DB_PASSWORD`, and `SMS_BOOTSTRAP_SECRET`. Never commit values.
4. Compile on Windows using `.\mvnw.cmd -DskipTests compile`.
5. Start `SchoolManagementSystemApplication` in IntelliJ.
6. Open `http://localhost:8080/sms.html` if your backend starts successfully. No claim is made that these steps have been independently verified in this repository.

## Six-member development

See [TEAM_ROLES](docs/TEAM_ROLES.md) and [CONTRIBUTING](CONTRIBUTING.md).
- Open a GitHub Issue first.
- Work in a focused feature branch.
- Commit actual work from your own GitHub identity.
- Open a PR with code changes and tests.
- Obtain review from a different team member before merging to `main`.
- Keep existing class names and public contracts unless a reviewed change requires otherwise.

## Security and privacy

No real student records, MySQL credentials, bootstrap secrets, session data, uploaded documents, local IDE directories, compiled files, or exported Git histories may be committed. Check [SECURITY.md](SECURITY.md). **Current repository visibility may be public:** the owner should select private visibility in repository settings if required.

## Academic integrity

The commit history shows who made specific changes, not who originally wrote earlier code. All members should make and explain genuine contributions; disclose AI assistance in accordance with university guidance.

## Project status

See [IMPORT_CHECKLIST](docs/IMPORT_CHECKLIST.md). Baseline source import, successful CI, integrated testing and collaborator assignments will be verified separately.
