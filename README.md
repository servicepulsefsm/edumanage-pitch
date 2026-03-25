# Smart School — School Management System

A comprehensive school management platform for academic institutions, covering academics, administration, finance, communication, and student welfare.

## Overview

Smart School is a School Management System (SMS) that:
- Manages the complete student lifecycle from admission to graduation
- Tracks academic performance across terms, subjects, and examinations
- Handles financial operations including fees, payments, and accounting
- Provides communication channels between school, teachers, and parents
- Manages student welfare including health, transport, hostel, and sports

## Key Design Principles

| Principle | Implementation |
|-----------|----------------|
| **Role-based access** | Each user type sees only what they need |
| **Parent visibility** | Parents have real-time visibility into their child's academic life |
| **Teacher autonomy** | Teachers manage their own classes, attendance, and assessments |
| **Admin as control plane** | All configuration, approvals, and system settings flow through admin |
| **Data isolation** | Students/parents see only their own data; teachers see only their classes |
| **Academic calendar driven** | Everything ties back to academic years, terms, and timetables |

## Documentation

| Document | Description |
|----------|-------------|
| [Actors & Roles](docs/actors-and-roles.md) | User roles, permissions, and data boundaries |
| [Module Reference](docs/module-reference.md) | All 32 modules with scope and features |
| [Product Roadmap](docs/product-roadmap.md) | Prioritized feature backlog (RICE scored) |
| [Workflows](docs/workflows.md) | Key process flows (admissions, examinations, fees) |

## Student Lifecycle

```
Enquiry → Application → Admission → Enrollment → Academic Years
    → Attendance → Examinations → Report Cards → Promotion/Graduation
```

## System Modules

| Category | Modules |
|----------|---------|
| **Academics** | Academic Years, Classes, Subjects, Syllabus, Examinations, Quizzes, Timetable |
| **People** | Students, Teachers, Staff, Parents |
| **Finance** | Fees, Payments, Accounting, Financial Reports |
| **Communication** | Messaging, Notifications, Announcements |
| **Administration** | Departments, Admissions, Certificates, ID Cards, Settings |
| **Student Life** | Sports, Health, Hostel, Transport, Library |
| **Safety** | Incident Reporting and Management |
| **Assets** | School Property and Inventory Management |
| **Reports** | Analytics, Performance Reports, Dashboards |

## Source Code

- **Lovable project**: https://lovable.dev/projects/a29dc1f7-d3da-4c56-8202-18a4a90dabee
- **GitHub repo**: https://github.com/servicepulsefsm/smart-school-smile
- **Supabase project**: EduManage School (`qynaggzhdrcyfrnkcbbv`)

## License

Proprietary — Anaiah
