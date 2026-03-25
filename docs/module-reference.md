# Smart School — Module Reference
**Version:** 1.0
**Scope:** Complete module inventory with features, data ownership, and access rules

---

## Module Categories

### Category 1: Academics

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Academic Years | `AcademicYears.tsx` | Admin | Define academic years, terms/semesters, set active year |
| Classes | `Classes.tsx` | Admin | Create classes/sections, assign class teachers, set capacity |
| Subjects | `Subjects.tsx` | Admin | Define subjects, assign to classes, assign teachers |
| Syllabus | `Syllabus.tsx` | Admin/Teacher | Track curriculum coverage per subject per term |
| Examinations | `Examinations.tsx` | Admin/Teacher | Create exams, enter grades, configure grading scales |
| Quizzes | `Quizzes.tsx` | Teacher | Create and manage class quizzes and assessments |
| Timetable | `Timetable.tsx` | Admin | Master timetable — period allocation per class |
| Student Timetable | `StudentTimetable.tsx` | Student/Teacher | Individual view of class schedule |
| My Subjects | `MySubjects.tsx` | Teacher | Teacher's view of assigned subjects and classes |

---

### Category 2: People Management

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Students | `Students.tsx` | Admin | Student records — enrollment, profile, academic history |
| Teachers | `Teachers.tsx` | Admin | Teacher profiles, qualifications, class assignments |
| Staff | `Staff.tsx` | Admin | Non-teaching staff — admin, maintenance, support |
| Parents | `Parents.tsx` | Admin | Parent/guardian profiles, linked to students |

#### Key Relationships
```
Parent ──has──▶ Student(s)
Student ──enrolled in──▶ Class
Class ──has──▶ Subject(s)
Subject ──taught by──▶ Teacher
Teacher ──assigned to──▶ Class(es)
Department ──contains──▶ Subject(s) + Teacher(s)
```

---

### Category 3: Finance

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Finance | `Finance.tsx` | Admin/Finance | Fee structures, payment tracking, accounting, reports |

#### Finance Sub-Features
| Feature | Description |
|---------|-------------|
| Fee Structures | Define fee types per class/term (tuition, boarding, transport, etc.) |
| Payment Recording | Record cash, bank, mobile money payments |
| Outstanding Balances | Per-student balance tracking with aging |
| Fee Reminders | Automated notifications to parents for overdue fees |
| Financial Reports | Collection summaries, outstanding reports, revenue analysis |
| Receipts | Generate and issue payment receipts |

---

### Category 4: Communication

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Communication | `Communication.tsx` | Admin/Teacher | Messaging, announcements, notifications |

#### Communication Channels
| Channel | Use Case |
|---------|----------|
| In-app messaging | Teacher ↔ Parent, Admin → All |
| Announcements | School-wide or class-specific notices |
| Notifications | Automated alerts (attendance, fees, grades) |
| SMS (future) | Critical alerts and fee reminders |

---

### Category 5: Administration

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Departments | `Departments.tsx` | Admin | Academic departments (Sciences, Languages, etc.) |
| Admissions | `Admissions.tsx` | Admin | Application processing, enrollment workflow |
| Certificates | `Certificates.tsx` | Admin | Generate leaving certificates, achievement certificates |
| ID Cards | `IDCards.tsx` | Admin | Student and staff ID card generation |
| Settings | `SettingsPage.tsx` | Admin | System configuration, school info, academic config |

#### Admissions Workflow
```
Enquiry → Application Form → Document Submission → Review
    → Entrance Assessment (optional) → Acceptance/Rejection
    → Fee Payment → Enrollment → Class Assignment
```

---

### Category 6: Student Life

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Sports | `Sports.tsx` | Admin/Coach | Sports teams, events, fixtures, results |
| Health | `Health.tsx` | Admin/Nurse | Student health records, medical visits, allergies |
| Hostel | `Hostel.tsx` | Admin/Warden | Room allocation, hostel rules, attendance |
| Transport | `Transport.tsx` | Admin | Bus routes, vehicle tracking, student assignments |
| Library | `LibraryPage.tsx` | Admin/Librarian | Book catalogue, borrowing, returns, fines |

---

### Category 7: Safety & Compliance

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Incidents | `Incidents.tsx` | Admin | Disciplinary incidents, accident reports, follow-up |

#### Incident Types
| Type | Description |
|------|-------------|
| Disciplinary | Behavioral issues, rule violations |
| Accident | Injuries, medical emergencies |
| Property | Damage to school property |
| Bullying | Reported bullying incidents |
| General | Other incidents requiring documentation |

---

### Category 8: Assets & Inventory

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Assets | `Assets.tsx` | Admin | School property — furniture, equipment, vehicles |

---

### Category 9: Reports & Analytics

| Module | Page | Owner | Description |
|--------|------|-------|-------------|
| Reports | `Reports.tsx` | Admin | Consolidated analytics and report generation |

#### Report Types
| Report | Audience | Description |
|--------|----------|-------------|
| Academic Performance | Admin, HOD | Class averages, subject trends, top/bottom performers |
| Attendance Summary | Admin, Teacher | Daily/weekly/term attendance rates |
| Financial Summary | Admin, Finance | Fee collection, outstanding, revenue |
| Teacher Workload | Admin | Teaching hours, class distribution |
| Student Demographics | Admin | Enrollment stats, gender ratio, class sizes |
| Exam Analysis | Admin, Teacher | Pass rates, grade distribution per subject |

---

## Shared Components

| Component | Location | Description |
|-----------|----------|-------------|
| `DashboardLayout.tsx` | Layout wrapper | Main layout with sidebar navigation |
| `AppSidebar.tsx` | Navigation | Role-based sidebar menu |
| `DashboardHeader.tsx` | Header | Top bar with user info, notifications |
| `StatCard.tsx` | Widget | Reusable dashboard statistics card |
| `PagePlaceholder.tsx` | Placeholder | Empty state for unimplemented modules |

### Component Subdirectories
| Directory | Description |
|-----------|-------------|
| `dashboards/` | Role-specific dashboard views |
| `finance/` | Finance-specific components |
| `incidents/` | Incident management components |
| `sports/` | Sports management components |
| `subjects/` | Subject-related components |
| `timetable/` | Timetable components |
| `teacher-dashboard/` | Teacher portal components |
| `parent-dashboard/` | Parent portal components |
| `report-cards/` | Report card generation components |
| `shared/` | Shared/reusable components |
| `ui/` | shadcn/ui base components |
