# Architecture notes from uploaded project

**Source reviewed:** User-provided Spring Boot project archive, not an independently verified running server.

## Runtime flow

`SchoolManagementSystemApplication.main` → Spring Boot → security filters/controllers → services/JPA repositories and JdbcTemplate → MySQL.

The legacy `School_MS.main` delegates to `SchoolManagementSystemApplication.main`; do not introduce a second independent Spring Boot entry point.

## Java package

`src/main/java/SchoolManagementSystem/` contains:
- Entities, Spring Data repositories and services for Student, Teacher, StudentProfile, Grade, Attendance, SubjectMarks, AssignmentMarks, TeacherAssignment, PhysicalProperties, NonAcademic and admissions.
- The newer `Sms*` controllers for authentication, admin workflows, teacher workflows, assignments and admission rules.
- `SmsSecurityConfig` and `SmsAccessService` to support role and scope checks.

## Frontend

The uploaded archive contains `index.html` / `app.js` / `styles.css` and equivalent `sms.html` / `sms.js` / `sms.css` under `src/main/resources/static/`.
Check security mappings before changing default login URLs; `sms.html` is permitted for unauthenticated users while `index.html` is restricted in the current uploaded security configuration.

## Backend routes

- `/api/auth/*`: first-admin setup, login, status and session-related operations.
- `/api/admin/*`: administrative management.
- `/api/teacher/*`: teacher operations with scopes.
- Other endpoints also exist in `SmsAdmissionsController` and `SmsAssignmentController`; verify the exact per-method mappings when implementing changes.

## Important integration checks

1. Confirm all expected database tables exist in a clean database.
2. Test first-admin bootstrap and verify it cannot be repeated.
3. Test admin vs teacher permissions using backend requests.
4. Ensure student/grade ID mapping and marks foreign keys are correct.
5. Test admissions capacity under boundary conditions and concurrency.
6. Verify no raw JSON or sensitive response data leaks unintentionally to the UI.
7. Run Maven compilation; unit/integration tests must be expanded.

This document is intentionally descriptive; it does not assert all modules are bug-free.
