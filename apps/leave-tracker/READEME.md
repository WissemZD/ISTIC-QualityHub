# 🗓️ Leave Tracker — Suivi des Congés & Présence

> Staff HR Management · ISO 21001:2018 · Standalone HTML Application

[![Version](https://img.shields.io/badge/Status-Planned-lightgrey?style=flat-square)](#)
[![ISO 21001](https://img.shields.io/badge/ISO%2021001-2018-blue?style=flat-square)](https://www.iso.org/standard/66266.html)

---

## 📋 Overview / Description

**EN** — A staff attendance and leave management application for university departments. Track leave requests, manage leave balances by type, visualize team presence planning, and monitor attendance — all without any backend infrastructure.

**FR** — Une application de gestion des congés et de la présence du personnel pour les départements universitaires. Suivez les demandes de congé, gérez les soldes par type, visualisez le planning de présence de l'équipe et surveillez les absences — sans aucune infrastructure backend.

---

## 🎯 Target Users / Utilisateurs ciblés

- 👨‍💼 Department heads — Chefs de département
- 🧑‍💻 HR administrators — Responsables RH
- 👩‍🏫 Teaching and administrative staff — Personnel enseignant et administratif

---

## ✨ Planned Features / Fonctionnalités prévues

### Staff Management
- [ ] Staff directory with function, department, contract type
- [ ] Leave balance per staff member per leave type
- [ ] Annual balance initialization and carry-over

### Leave Types / Types de congé
- [ ] Annual leave — Congé annuel
- [ ] Sick leave — Congé maladie (with medical certificate tracking)
- [ ] Special leave — Congé exceptionnel (marriage, bereavement, etc.)
- [ ] Compensatory leave — Récupération
- [ ] Maternity / Paternity leave
- [ ] Administrative absence — Absence administrative

### Leave Request Workflow
- [ ] Submit leave request with date range, type, justification
- [ ] Approval workflow: Pending → Approved / Rejected
- [ ] Automatic balance deduction on approval
- [ ] Overlap detection (prevent double booking)

### Presence & Attendance
- [ ] Daily attendance input (present / absent / remote)
- [ ] Monthly attendance summary per employee
- [ ] Absence rate calculation
- [ ] Late arrival / early departure tracking

### Planning View
- [ ] Monthly team calendar — who is present / on leave / absent
- [ ] Color-coded visual planning by leave type
- [ ] Department filter

### Dashboard & Reports
- [ ] Leave balance status per staff member
- [ ] Absence rate by department
- [ ] Monthly leave consumption chart
- [ ] Staff with most remaining balance (year-end alert)
- [ ] Export monthly attendance report (PDF / Excel)

---

## 📐 ISO 21001 Mapping / Correspondance ISO 21001

| Feature | ISO 21001:2018 |
|---|---|
| Staff competence & availability | §7.1.2 — Human resources |
| Training leave tracking | §7.2 — Competence |
| Attendance monitoring | §9.1 — Monitoring & measurement |
| HR records (leave history) | §7.5 — Documented information |

---

## 📁 Versions

| Version | File | Status |
|---|---|---|
| **v1.0** | `v1.0/LeaveTracker_v1.html` | 📋 Planned |

---

## 🗺️ Roadmap

- [ ] v1.0 — Staff directory, leave types, leave requests, balance tracking
- [ ] v1.1 — Attendance input, monthly presence calendar
- [ ] v1.2 — Dashboard with absence rates, team planning view
- [ ] v2.0 — Full reports module, PDF/Excel export

---

*Part of [ISTIC-QualityHub](../../README.md) — Back to suite / Retour à la suite*
