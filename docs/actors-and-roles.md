# Smart School — Actors, Roles & Permissions
**Version:** 1.0
**Scope:** Who does what, when, and what they can see
**Approach:** Jobs-to-be-Done framework aligned with school operations

---

## 1. System Boundary (What This System Does)

| IN SCOPE | OUT OF SCOPE |
|----------|--------------|
| Student enrollment and records | Government regulatory submissions |
| Academic calendar and timetable management | External exam board integration (ZIMSEC, Cambridge) |
| Attendance tracking (students and staff) | Payroll processing (HR/finance system) |
| Examination creation, grading, and report cards | Online learning / LMS content delivery |
| Fee management and payment tracking | Bank payment gateway processing |
| Parent-school communication | Marketing and student recruitment CRM |
| Library, hostel, transport management | Facility maintenance (see ServicePulse) |
| Incident reporting and health records | Medical treatment / clinical records |
| Sports and extracurricular tracking | |
| Asset and inventory management | |
| Certificate and ID card generation | |
| **Reporting & Analytics** | |
| — Student performance trends | |
| — Attendance analytics | |
| — Financial summaries | |

> **North Star:** Each role sees exactly what they need — nothing more, nothing less. Admin has full visibility. Teachers see their classes. Parents see their children. Students see their own records. Accountability is clear within each boundary.

---

## 2. Design Principles (Non-Negotiable)

| Principle | Why It Matters |
|-----------|----------------|
| **Strict data isolation** | Parent A never sees Parent B's children. Teacher A only sees classes assigned to them. Students see only their own records. |
| **Admin is the control plane** | All configuration, user management, and system settings flow through admin |
| **Financial data restricted** | Fee structures visible to admin and finance. Parents see only their own balances. Teachers have no access to financials. |
| **Teachers own their classroom** | Attendance, grades, and subject content are managed by the assigned teacher |
| **Parents are observers, not operators** | View-only access to their child's academic life — cannot modify records |
| **Academic calendar is the backbone** | Terms, semesters, and academic years drive everything — attendance, exams, fees, reports |

---

## 3. Data Isolation Model

### User Boundaries

| User Type | Isolation Boundary | Description |
|-----------|-------------------|-------------|
| **Admin** | None (full visibility) | Sees all students, teachers, classes, finances, reports |
| **Teacher** | Assigned Classes + Subjects | Sees only students in their classes and subjects they teach |
| **Parent** | Child IDs | Sees only their own children's records across all modules |
| **Student** | Own User ID | Sees only their own attendance, grades, timetable, and notices |
| **Finance Officer** | Financial data only | Fee structures, payments, accounting — no academic records |
| **Librarian** | Library module only | Book inventory, borrowing records |
| **Hostel Warden** | Hostel module only | Room assignments, hostel attendance |

### Organization Hierarchy

```
┌─────────────────────────────────────────────────────────┐
│                    SCHOOL ADMIN                          │
│              (Full control — all modules)                │
└─────────────────────────┬───────────────────────────────┘
                          │
          ┌───────────────┼───────────────┐
          ▼               ▼               ▼
   ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
   │  ACADEMIC   │ │  FINANCE    │ │ OPERATIONS  │
   │  STAFF      │ │  STAFF      │ │  STAFF      │
   │             │ │             │ │             │
   │ Teachers    │ │ Fee Mgmt    │ │ Library     │
   │ HODs        │ │ Payments    │ │ Hostel      │
   │ Exam Coord  │ │ Accounting  │ │ Transport   │
   └──────┬──────┘ └─────────────┘ │ Sports      │
          │                        │ Health      │
          ▼                        └─────────────┘
   ┌─────────────┐
   │  STUDENTS   │
   │  & PARENTS  │
   │             │
   │ View own    │
   │ records     │
   └─────────────┘
```

---

## 4. Roles & Permissions

### Role: `school_admin` — School Administrator

> Full system access — manages all configuration, users, and operations

#### Navigation Access
- Dashboard (all stats)
- All modules (32 pages)
- Settings (all configuration)

#### Permissions
| Area | Actions |
|------|---------|
| Students | Create, edit, view, delete, promote, transfer |
| Teachers | Create, edit, view, assign classes/subjects |
| Staff | Create, edit, view all staff types |
| Parents | Create, edit, view, link to students |
| Academic Years | Create, configure terms, set active year |
| Classes | Create, assign teachers, manage sections |
| Subjects | Create, assign to classes and teachers |
| Timetable | Create, edit, publish |
| Examinations | Create exam schedules, configure grading |
| Finance | Full access — fees, payments, reports |
| Admissions | Manage applications, approve/reject |
| Reports | All reports — academic, financial, attendance |
| Settings | System configuration, branding, notifications |

---

### Role: `teacher` — Teacher

> Manages their assigned classes — attendance, grades, and subject content

#### Navigation Access
- Dashboard (own classes)
- My Subjects
- Student Timetable
- Attendance (own classes)
- Examinations (own subjects)

#### Permissions
| Area | Actions |
|------|---------|
| Attendance | Mark attendance for assigned classes |
| Examinations | Enter grades for assigned subjects |
| Quizzes | Create and grade quizzes for assigned subjects |
| Students | View student profiles (own classes only) |
| Timetable | View own timetable |
| Communication | Send messages to parents of students in own classes |
| Report Cards | Generate and review for own students |

#### Cannot Access
- Finance, Admissions, Settings, HR, Assets
- Other teachers' classes or grades
- System configuration

---

### Role: `parent` — Parent / Guardian

> View-only access to their children's academic life

#### Navigation Access
- Parent Dashboard
- Child's Attendance
- Child's Grades / Report Cards
- Fee Statements
- Communication (with school/teachers)

#### Permissions
| Area | Actions |
|------|---------|
| Student Profile | View own child's profile |
| Attendance | View own child's attendance records |
| Grades | View own child's examination results |
| Report Cards | View and download own child's report cards |
| Fees | View fee balance, payment history |
| Communication | Send/receive messages with school |
| Timetable | View own child's class timetable |

#### Cannot Access
- Other students' data
- Teacher tools, admin settings
- Financial management (only own balances)

---

### Role: `student` — Student

> View-only access to own academic records

#### Navigation Access
- Student Dashboard
- My Timetable
- My Subjects
- My Grades

#### Permissions
| Area | Actions |
|------|---------|
| Timetable | View own class timetable |
| Subjects | View enrolled subjects |
| Grades | View own examination results |
| Attendance | View own attendance record |
| Library | View borrowed books, request books |
| Quizzes | Take assigned quizzes |

---

### Role: `finance_officer` — Finance Staff

> Manages fees, payments, and financial reporting

#### Navigation Access
- Finance Dashboard
- Fee Management
- Payment Tracking
- Financial Reports

#### Permissions
| Area | Actions |
|------|---------|
| Fees | Create fee structures, assign to classes |
| Payments | Record payments, issue receipts |
| Reports | Generate financial reports, outstanding balances |
| Students | View student list (for fee assignment only) |

#### Cannot Access
- Academic records, grades, attendance
- System settings, user management

---

### Role: `department_head` — Head of Department

> Teacher with additional oversight of their department's academic performance

#### Permissions (in addition to Teacher)
| Area | Actions |
|------|---------|
| Department | View all teachers and classes in department |
| Examinations | Review grades across department subjects |
| Reports | Department-level academic performance reports |
| Syllabus | Approve syllabus coverage for department subjects |
