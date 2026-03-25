# Smart School — Key Workflows
**Version:** 1.0
**Scope:** End-to-end process flows for core school operations

---

## 1. Admissions Workflow

```
Parent Enquiry → Application Form Submitted → Documents Uploaded
        ↓
    Admin Reviews Application
        ↓
    ┌──────────┬───────────────┐
    ↓          ↓               ↓
 Accepted   Waitlisted      Rejected
    ↓          ↓               ↓
 Fee Payment  Notify Parent   Notify Parent
    ↓                          (end)
 Enrollment Confirmed
    ↓
 Class Assignment
    ↓
 Student Record Created
    ↓
 Parent Account Linked
    ↓
 Welcome Pack Sent (ID Card, Timetable, Fee Structure)
```

### Admission Statuses

| Status | Description | Next Actions |
|--------|-------------|--------------|
| `enquiry` | Initial contact — no application yet | Submit application |
| `application_submitted` | Application form and documents received | Admin review |
| `under_review` | Admin is evaluating the application | Accept, reject, or waitlist |
| `assessment_scheduled` | Entrance test/interview scheduled | Complete assessment |
| `accepted` | Offer extended to parent | Pay fees |
| `waitlisted` | On waiting list — space dependent | Promote or reject |
| `rejected` | Application declined | End |
| `fees_paid` | Initial fees received | Complete enrollment |
| `enrolled` | Fully enrolled — student is active | Academic lifecycle begins |

---

## 2. Academic Year Workflow

```
Admin Creates Academic Year (e.g., 2026)
        ↓
    Defines Terms (Term 1, Term 2, Term 3)
        ↓
    Sets Term Dates (start, end, exam periods)
        ↓
    Creates/Updates Class List
        ↓
    Assigns Teachers to Classes & Subjects
        ↓
    Generates Timetable
        ↓
    Publishes — Year is ACTIVE
        ↓
    ══════════════════════════════
    ║  Daily operations begin   ║
    ══════════════════════════════
        ↓
    Term 1 → Exams → Report Cards → Term Break
        ↓
    Term 2 → Exams → Report Cards → Term Break
        ↓
    Term 3 → Final Exams → Annual Report Cards
        ↓
    Promotion/Retention Process
        ↓
    Year Closed — Archive
```

---

## 3. Examination Workflow

```
Admin/Teacher Creates Exam Schedule
        ↓
    Defines: Subject, Date, Duration, Max Marks, Weightage
        ↓
    Exam Conducted (offline)
        ↓
    Teacher Enters Marks per Student
        ↓
    System Auto-Calculates:
    — Percentage
    — Grade (based on grading scale)
    — Class rank
    — Subject average
        ↓
    HOD/Admin Reviews (optional)
        ↓
    Report Cards Generated
        ↓
    ┌──────────────────────────────────┐
    │  Report Card Contains:            │
    │  — Subject-wise marks & grades    │
    │  — Term average / GPA             │
    │  — Class rank                     │
    │  — Teacher comments               │
    │  — Attendance summary             │
    │  — Conduct/behavior remarks       │
    │  — Principal's remarks            │
    └──────────────────────────────────┘
        ↓
    Published to Parent Portal
        ↓
    Parent Views / Downloads
```

### Exam Statuses

| Status | Description |
|--------|-------------|
| `draft` | Exam created but not finalized |
| `scheduled` | Dates confirmed, visible to teachers |
| `in_progress` | Exam period is active |
| `marking` | Exams complete, teachers entering marks |
| `review` | Marks entered, pending HOD/admin review |
| `published` | Results published to students/parents |

---

## 4. Fee Collection Workflow

```
Admin Creates Fee Structure for Class + Term
        ↓
    Fee Assigned to Students (bulk or individual)
        ↓
    Parent Receives Fee Statement (notification)
        ↓
    Parent Makes Payment (cash/bank/mobile)
        ↓
    Finance Records Payment
        ↓
    Receipt Generated & Sent to Parent
        ↓
    Balance Updated in Real-Time
        ↓
    If Outstanding > 0:
        ↓
    ┌──────────────────────────────┐
    │  Automated Reminder Sequence │
    │  Day 7:  Gentle reminder     │
    │  Day 30: Firm reminder       │
    │  Day 60: Final notice        │
    │  Day 90: Escalation to admin │
    └──────────────────────────────┘
```

### Payment Statuses

| Status | Description |
|--------|-------------|
| `not_due` | Fee assigned but term hasn't started |
| `due` | Payment expected — term active |
| `partially_paid` | Some amount received, balance remaining |
| `paid` | Full amount received |
| `overdue` | Past due date, no/insufficient payment |
| `waived` | Fee waived (scholarship, special case) |

---

## 5. Daily Attendance Workflow

```
School Day Starts
        ↓
    Teacher Opens Class Attendance
        ↓
    Marks Each Student: Present / Absent / Late / Excused
        ↓
    Submits Attendance
        ↓
    System Checks Absent Students:
        ↓
    ┌─────────────────────────────────┐
    │  For each ABSENT student:        │
    │  → Send notification to parent   │
    │  → Update attendance record      │
    │  → Check cumulative absence      │
    │  → If threshold exceeded:        │
    │    → Flag for admin attention    │
    └─────────────────────────────────┘
        ↓
    Attendance Visible on:
    — Teacher dashboard (class view)
    — Parent portal (child view)
    — Admin reports (school-wide)
```

---

## 6. Incident Reporting Workflow

```
Incident Occurs (disciplinary, accident, bullying, etc.)
        ↓
    Teacher/Staff Logs Incident
        ↓
    Details: Student(s), Type, Severity, Description, Witnesses
        ↓
    Admin Notified
        ↓
    ┌──────────────────┐
    │  Severity Check   │
    ├──────────────────┤
    │ Low → Teacher     │
    │       handles     │
    │                   │
    │ Medium → Admin    │
    │          reviews  │
    │          + Parent │
    │          notified │
    │                   │
    │ High → Admin +    │
    │        Parent +   │
    │        Meeting    │
    │        scheduled  │
    └──────────────────┘
        ↓
    Resolution Documented
        ↓
    Follow-up Actions Assigned (if any)
        ↓
    Incident Closed
        ↓
    Added to Student Conduct History
```
