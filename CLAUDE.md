# EduManage — School Management System

## Project Overview
**EduManage is not a School Management System. It is a reassurance engine — a single system of record across the full school management lifecycle, from admissions to graduation, that surfaces the right insight, for the right person, at the right moment. Every parent informed, every teacher equipped, every student organized, every school accountable.**

### How It Works — Four Layers, One System

**Layer 1 — System of Record.** Everything starts here. Admissions, attendance, grades, fees, timetables, communications, conduct, sports — the complete school operation captured in one place. This is what the school runs on daily. It replaces fragmented spreadsheets, paper registers, and personal WhatsApp groups with a single source of truth that every downstream layer draws from.

**Layer 2 — Contextual Reassurance.** The system of record is useless if only the admin sees it. EduManage surfaces contextually relevant insights to each stakeholder — parents see their child's week, teachers see their classroom, students see their schedule and progress, finance sees cash flow, school leadership sees the whole picture. Not a data dump. Each person gets what they need to know and what to do next. This is where reassurance lives — the parent doesn't call the school, the teacher doesn't repeat themselves, the student knows what's coming.

**Layer 3 — Intelligence.** Over time, the system of record compounds into something more powerful than daily operations:
- **Student profiles** — every academic result, attendance pattern, sports participation, behavioural record, and communication is woven into a comprehensive profile that surfaces the whole child. Academic performance, emotional intelligence, social engagement, behavioural patterns — not just grades. Teachers use it to give personalised attention. Parents see the full picture and can guide their child toward the strengths, interests, and career path where they are most likely to thrive.
- **Teacher performance profiles** — syllabus coverage, student outcomes, attendance patterns, parent feedback. Performance reviews become evidence-based, not subjective. The goal is not surveillance but continuous improvement — helping teachers get better, which ultimately raises the quality of students the school produces.
- **AI-assisted financial reconciliation** — fees come in via mobile money, bank transfers, and cash. Expenses go out to suppliers, staff, and service providers. AI automatically reconciles accounts payable and accounts receivable, matching payments to invoices, flagging discrepancies, and giving the finance office a clean, real-time picture of the school's financial health without manual spreadsheet work.

**Layer 4 — Governance & Compliance.** Schools report to governing authorities — ministry of education, school boards, regulatory bodies. EduManage generates compliance and performance reports that can be submitted directly, pulling from the same system of record. No separate data collection exercise. The data is already there because Layers 1-3 captured it as part of daily operations.

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
