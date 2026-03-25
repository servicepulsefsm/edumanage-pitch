# Smart School — Product Roadmap
**Version:** 1.0
**Methodology:** RICE scoring (Reach × Impact × Confidence ÷ Effort)

A prioritized feature backlog grouped into strategic themes. The goal is to build a comprehensive school management platform that handles the full academic lifecycle.

---

### How RICE Scoring Works

| Factor | Scale | Meaning |
|--------|-------|---------|
| **Reach** | 1–10 | How many users/stakeholders does this touch? |
| **Impact** | 1–10 | How much does it move the needle for those users? |
| **Confidence** | 1–10 | How sure are we about reach and impact estimates? |
| **Effort** | 1–10 | How many person-months to build? (higher = harder) |
| **Score** | (R × I × C) ÷ E | Higher is better |

---

### THEME 1: Core Academic Lifecycle

| Feature | Motivation | Stakeholders | R | I | C | E | Score |
|---------|-----------|--------------|---|---|---|---|-------|
| Report card generation with term/annual aggregation | Auto-generate report cards from examination results with class rankings, teacher comments, and term/annual averages — replacing manual Excel-based report cards. Parents receive digital copies instantly. | Admin, Teachers, Parents | 10 | 10 | 9 | 5 | 18.0 |
| Grading scale configuration per academic year | Define custom grading scales (A-F, percentage-based, GPA) per year/class level with automatic grade mapping from raw scores. Different scales for primary vs secondary. | Admin, Teachers | 9 | 8 | 9 | 3 | 21.6 |
| Student promotion and retention workflow | End-of-year process to promote students to next class, retain, or transfer — with configurable pass/fail criteria, bulk operations, and parent notifications. | Admin, Teachers, Parents | 9 | 9 | 8 | 5 | 12.96 |
| Syllabus coverage tracking with teacher self-reporting | Teachers log syllabus completion per topic per term. HODs and admin have visibility into coverage rates across subjects. Early warning when coverage falls behind. | Teachers, HODs, Admin | 8 | 7 | 7 | 4 | 9.8 |
| Class stream/section management | Split classes into streams (e.g., Form 2A, 2B, 2C) with independent timetables, teachers, and grade books. Supports both mixed-ability and streamed groupings. | Admin, Teachers | 8 | 7 | 8 | 4 | 11.2 |

---

### THEME 2: Attendance & Discipline

| Feature | Motivation | Stakeholders | R | I | C | E | Score |
|---------|-----------|--------------|---|---|---|---|-------|
| Daily attendance with parent auto-notification | Teacher marks attendance per class. Absent students' parents receive instant SMS/notification. Weekly and term summaries available to admin. | Teachers, Parents, Admin | 10 | 9 | 9 | 4 | 20.25 |
| Staff attendance and leave management | Track teacher/staff attendance, manage leave requests and approvals, calculate days present per month for payroll reference. | Admin, Staff | 8 | 7 | 8 | 5 | 8.96 |
| Incident management with parent notification | Log disciplinary incidents with severity levels, link to students, notify parents, track resolution and follow-up actions. Build a student conduct history. | Admin, Teachers, Parents | 8 | 8 | 7 | 4 | 11.2 |
| Late arrival tracking | Record students arriving late separately from absent — with cumulative tracking and automated warnings when thresholds are exceeded. | Teachers, Admin, Parents | 7 | 6 | 8 | 3 | 11.2 |

---

### THEME 3: Finance & Fees

| Feature | Motivation | Stakeholders | R | I | C | E | Score |
|---------|-----------|--------------|---|---|---|---|-------|
| Fee structure templates per class and term | Define fee breakdowns (tuition, boarding, transport, lab fees, etc.) per class per term. Assign to students individually or in bulk. Supports scholarships and discounts. | Admin, Finance, Parents | 9 | 9 | 9 | 5 | 14.58 |
| Payment recording with receipt generation | Record payments (cash, bank transfer, mobile money), auto-generate receipts, update balances in real-time. Parents see updated statements instantly. | Finance, Parents | 9 | 8 | 9 | 4 | 16.2 |
| Outstanding balance dashboard with aging | Real-time view of all outstanding fees with 30/60/90-day aging. Filter by class, term, or individual student. Export for finance team. | Admin, Finance | 8 | 8 | 8 | 3 | 17.07 |
| Automated fee reminders to parents | Scheduled SMS/notification reminders for overdue fees with escalation tiers (gentle → firm → final notice). Configurable thresholds and messaging. | Finance, Parents | 8 | 7 | 7 | 4 | 9.8 |
| Financial period reports | Term and annual financial summaries — total collected, outstanding, revenue by category, comparison across terms/years. | Admin, Finance | 7 | 7 | 8 | 4 | 9.8 |

---

### THEME 4: Communication & Engagement

| Feature | Motivation | Stakeholders | R | I | C | E | Score |
|---------|-----------|--------------|---|---|---|---|-------|
| School-wide and class-specific announcements | Admin and teachers publish announcements to all parents, specific classes, or individual parents. With read receipts and pinned notices. | Admin, Teachers, Parents | 10 | 7 | 9 | 3 | 21.0 |
| Teacher-parent direct messaging | Secure in-app messaging between teachers and parents for individual student matters. Threaded conversations with history. | Teachers, Parents | 9 | 8 | 8 | 4 | 14.4 |
| SMS integration for critical notifications | Send attendance alerts, fee reminders, and emergency notices via SMS — critical for parents without smartphones or consistent internet. | Admin, Parents | 8 | 8 | 7 | 6 | 7.47 |
| Event calendar with RSVP | School events (sports days, parent meetings, exams) published to calendar. Parents can RSVP. Automated reminders before events. | Admin, Parents, Students | 8 | 6 | 7 | 4 | 8.4 |

---

### THEME 5: Student Welfare

| Feature | Motivation | Stakeholders | R | I | C | E | Score |
|---------|-----------|--------------|---|---|---|---|-------|
| Student health records with allergy alerts | Maintain medical history, allergies, chronic conditions, and emergency contacts. Teachers see allergy alerts for students in their classes. | Admin, Nurse, Teachers, Parents | 8 | 9 | 8 | 4 | 14.4 |
| Hostel room allocation and management | Assign students to rooms/dorms, track occupancy, manage hostel rules and attendance. Warden dashboard with room-level visibility. | Admin, Warden | 6 | 7 | 8 | 4 | 8.4 |
| Transport route management | Define bus routes, assign students, track vehicle allocation, communicate route changes to parents. | Admin, Parents | 7 | 6 | 7 | 4 | 7.35 |
| Library management with borrowing system | Book catalogue, student borrowing/returns, overdue tracking, fine calculation, reading history. | Librarian, Students | 6 | 5 | 8 | 4 | 6.0 |
| Sports team management and event tracking | Create teams, manage fixtures, record results, track student participation across sports. | Admin, Coach, Students | 5 | 5 | 7 | 3 | 5.83 |

---

### THEME 6: Reports & Intelligence

| Feature | Motivation | Stakeholders | R | I | C | E | Score |
|---------|-----------|--------------|---|---|---|---|-------|
| Student performance trend analysis | Track individual student performance across terms — identify improving, declining, and at-risk students. Visual trend charts for parent meetings. | Admin, Teachers, Parents | 9 | 9 | 8 | 5 | 12.96 |
| Class/subject comparative analytics | Compare class averages across subjects, identify weak areas, benchmark teacher effectiveness. | Admin, HODs | 8 | 8 | 7 | 5 | 8.96 |
| Attendance correlation with performance | Correlate attendance rates with academic performance to identify patterns — students with low attendance often underperform. | Admin, Teachers | 7 | 7 | 6 | 4 | 7.35 |
| Exportable reports (PDF, Excel) | One-click export of any report to PDF or Excel for board meetings, government submissions, and record-keeping. | Admin | 9 | 6 | 9 | 3 | 16.2 |
