# Six-member responsibility plan

All responsibilities below are **assignments for future work**, not claims of past authorship. Replace Member 2–6 with the collaborators' actual GitHub usernames after they confirm responsibilities.

| Member | Scope | Existing classes / source areas | Initial deliverable |
|---|---|---|---|
| **Member 1 / Maintainer** | Integration, login/security, configuration, reviews | `SchoolManagementSystemApplication`, `School_MS`, `SmsSecurityConfig`, `SmsAuthController`, `SmsAccessService` | Secure imports, auth tests, CI review |
| **Member 2** | Students and student profiles | `Student`, `StudentController`, `StudentService`, `StudentProfile`, `StudentProfileService` and repositories | Validation and profile lookup tests |
| **Member 3** | Teachers and permissions | `Teacher`, controllers/services/repos, teacher scope routes | Teacher registration checks and role/scope tests |
| **Member 4** | Academics | `Attendance`, `SubjectMarks`, `AssignmentMarks`, `TeacherAssignment` and associated classes | Attendance/marks/assignments tests |
| **Member 5** | Admissions | `AdmissionGrade1`, `AdmissionIntermediate`, `AdmissionAL`, `SmsAdmissionsController` | Capacity and priority-rule tests |
| **Member 6** | Properties, staff, frontend | `PhysicalProperties`, `NonAcademic`, `src/main/resources/static/` | Properties tests and accessible UI fixes |

### Shared responsibilities

- All members review at least one teammate's PR.
- The maintainer integrates and coordinates API/database contracts; this does **not** give the maintainer authorship of everyone else's changes.
- Keep original source names; avoid simultaneous conflicting edits to shared files like `SmsAdminController.java` and `application.properties`.
- For each task: linked issue → personal branch → actual commit(s) → PR → review → merge.
