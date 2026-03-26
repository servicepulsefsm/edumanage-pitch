# EduManage

## EduManage. Finally, nothing is hidden.

### Four Stakeholders. Four Categories. One Platform.

| Stakeholder | Category | One-liner |
|-------------|----------|-----------|
| **School Leadership** | School Performance Intelligence | Prove and improve your school — before the market decides for you |
| **Parent** | Parent Transparency Engine | Your child's day, growth, and the return on every fee you've paid |
| **Teacher** | Classroom Professional Intelligence | What's actually working — for each child, every term |
| **Student** | Lifelong Learner Record | From first day of school to first day of work |

---

### How It Works — Four Layers, One System

**Layer 1 — System of Record.** Admissions, attendance, grades, fees, timetables, communications, conduct, sports — the complete school operation in one place. Replaces fragmented spreadsheets, paper registers, and WhatsApp groups with a single source of truth.

**Layer 2 — Stakeholder Intelligence.** The system of record is useless if only school management sees it. EduManage surfaces contextually relevant insight to each stakeholder — school leaders see institutional performance, parents see their child's journey, teachers see their classroom effectiveness, students see their 360 profile. Not a data dump. Each person gets what they need to know and what to do next.

**Layer 3 — Compounding Intelligence.** Over time, the data compounds:
- **Lifelong student profiles** — academic, emotional, social, behavioural — the whole child, not just grades. The profile outlives the school: primary → secondary → university → employment. The child owns it.
- **School Performance Intelligence** — cohort trajectories, teacher effectiveness tied to student outcomes, parent confidence scoring, institutional reputation metrics. Leaders see whether the school is winning or slowly losing ground.
- **Classroom Professional Intelligence** — teachers get insight back from the data they put in. Which approaches are working? Which students are progressing? Evidence-based, not subjective.
- **AI financial reconciliation** — mobile money, bank transfers, cash. AP/AR matching, discrepancy flagging, real-time cash flow visibility for planning.
- **Parent Transparency Engine** — the return on every fee paid. Child's progress, activities, engagement, and growth visible without calling the school.

**Layer 4 — Governance & Compliance.** Ministry reports, board submissions, regulatory compliance — generated from the same system of record. No separate data collection. The data is already there.

---

### Competitive Positioning

EduManage creates a new category. Existing players occupy three separate, disconnected markets:
- **School ERPs** (PowerSchool, Classter, Fedena) — admin tools
- **Student portfolio/LMS tools** (Seesaw, ClassDojo) — instructional tools
- **Employment verification** (LinkedIn, credential platforms) — post-school

Nobody connects them. The child's story resets to zero at every transition. EduManage sits at the only point where all the raw data exists and builds a continuous record across the full lifecycle.

**Key Africa-specific competitors:** BlueBic (200+ African schools), Uzalynx (Kenya, M-Pesa integrated), MyEncore (cashless canteen, transport tracking). None emphasise compounding student profiles, school performance intelligence, or AI financial reconciliation.

**EduManage's moat:** Longitudinal data that compounds with time. A platform tracking a child from age 6 to 18 has something no competitor can replicate quickly.

**Four revenue streams:** Schools (operations), Parents (child profile/visibility), Universities (verified applicant records), Employers (background verification).

## Source Code
- **Lovable project**: https://lovable.dev/projects/a29dc1f7-d3da-4c56-8202-18a4a90dabee
- **GitHub repo**: https://github.com/servicepulsefsm/smart-school-smile
- **Previous repo** (disconnected): `mashapajfhp/school-harmony-hub`
- **Supabase project**: EduManage School, ID `qynaggzhdrcyfrnkcbbv`

## Tech Stack
- **Frontend**: React 18, TypeScript, Vite
- **UI**: Tailwind CSS, shadcn/ui (Radix primitives), Recharts
- **Backend**: Supabase (auth, database, edge functions)
- **State**: TanStack React Query
- **Routing**: React Router DOM v6

## Documentation

| Document | Description |
|----------|-------------|
| [README](README.md) | Project overview, principles, module summary |
| [Actors & Roles](docs/actors-and-roles.md) | User roles, permissions, data isolation model |
| [Module Reference](docs/module-reference.md) | All 32 modules — scope, features, ownership |
| [Product Roadmap](docs/product-roadmap.md) | RICE-scored feature backlog across 6 themes |
| [Workflows](docs/workflows.md) | End-to-end process flows (admissions, exams, fees, attendance, incidents) |
| [Blue Ocean Strategy](docs/blue-ocean-strategy.md) | Category-creating positioning, ERRC framework, adoption flywheel, competitive moat |

## App Modules (32 pages)
| Module | Page | Description |
|--------|------|-------------|
| Dashboard | Index.tsx | Main overview with stats |
| Academics | AcademicYears, Classes, Subjects, Syllabus, Examinations, Quizzes | Curriculum and assessment |
| People | Students, Teachers, Staff, Parents | User management |
| Scheduling | Timetable, StudentTimetable, MySubjects | Class scheduling |
| Finance | Finance | Fees, payments, accounting |
| Attendance | Attendance | Student/staff attendance |
| Communication | Communication | Messaging and notifications |
| Administration | Departments, Admissions, Certificates, IDCards, Settings | School operations |
| Student Life | Sports, Health, Hostel, Transport, LibraryPage | Extracurricular and welfare |
| Safety | Incidents | Incident reporting |
| Assets | Assets | School property management |
| Reports | Reports | Analytics and reporting |
| Auth | Login | Authentication |

## Key Roles
| Role | Access |
|------|--------|
| `school_admin` | Full system — all modules, settings, reports |
| `teacher` | Own classes — attendance, grades, quizzes, communication |
| `parent` | Own children — view grades, attendance, fees, messages |
| `student` | Own records — timetable, grades, library |
| `finance_officer` | Financial modules only |
| `department_head` | Teacher + department oversight |

## Development Notes
- App code lives in Lovable — frontend changes go through Lovable chat, NOT local file edits
- This folder is for **documentation only**, not source code
- Use `mcp__supabase__*` tools with project_id `qynaggzhdrcyfrnkcbbv` for database operations
- Do NOT use `mcp__claude_ai_FSM_Supabase__*` — that points to a different project
