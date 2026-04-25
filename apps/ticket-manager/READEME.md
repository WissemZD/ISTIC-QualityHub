# 🎫 Ticket Manager — Gestion des Demandes d'Intervention

> IT & Technical Support · ISO 21001:2025 · Standalone HTML Application

[![Version](https://img.shields.io/badge/Status-In%20Development-orange?style=flat-square)](#)
[![ISO 21001](https://img.shields.io/badge/ISO%2021001-2025-blue?style=flat-square)](https://www.iso.org/standard/66266.html)

---

## 📋 Overview / Description

**EN** — A ticketing system designed for IT and technical support teams in higher education institutions. Manage intervention requests, track SLA compliance, monitor technician workloads, and generate statistics dashboards — all in a single HTML file.

**FR** — Un système de tickets conçu pour les équipes de support informatique et technique des établissements d'enseignement supérieur. Gérez les demandes d'intervention, suivez la conformité aux SLAs, surveillez la charge des techniciens et générez des tableaux de bord statistiques — tout dans un seul fichier HTML.

---

## 🎯 Target Processes / Processus ciblés

- 🖥️ IT Infrastructure support (hardware, network, servers)
- 💻 Software support (installations, licenses, configurations)
- 🔧 Technical maintenance (equipment, facilities)
- 🔒 Security incidents
- 📋 Recurring scheduled tasks (backups, updates, maintenance)

---

## ✨ Planned Features / Fonctionnalités prévues

### Ticket Management
- [ ] Create tickets with category, priority, affected service
- [ ] Assign to technician / responsible person
- [ ] Track status: New → In Progress → Resolved → Closed
- [ ] SLA timer per ticket category (e.g. Critical = 4h, High = 24h)
- [ ] Attach notes and resolution comments
- [ ] Link recurring tasks to a schedule (backup, weekly checks...)

### Dashboard & Metrics
- [ ] Real-time stats: open / in-progress / closed / overdue
- [ ] Average resolution time by category and technician
- [ ] SLA compliance rate (% tickets resolved within deadline)
- [ ] Workload chart per technician
- [ ] Recurring tasks calendar with completion tracking
- [ ] Monthly trends chart

### Planning (Recurring Tasks)
- [ ] Define recurring tasks (daily / weekly / monthly)
- [ ] Auto-generate task instances on schedule
- [ ] Mark completion with timestamp and notes
- [ ] Missed task alerts on dashboard

### Export
- [ ] PDF report (monthly activity summary)
- [ ] Excel export (full ticket list with metrics)
- [ ] JSON backup / restore

---

## 📐 ISO 21001 Mapping / Correspondance ISO 21001

| Feature | ISO 21001:2018 |
|---|---|
| Service request management | §8.1 — Operational planning |
| SLA tracking | §9.1 — Monitoring & measurement |
| Technician workload | §7.1 — Resources |
| Recurring task planning | §8.5 — Production and service provision |
| Dashboard & statistics | §9.1.3 — Analysis and evaluation |

---

## 📁 Versions

| Version | File | Status |
|---|---|---|
| **v1.0** | `v1.0/TicketManager_v1.html` | 🚧 In development |

---

## 🗺️ Roadmap

- [ ] v1.0 — Core ticket management + basic dashboard
- [ ] v1.1 — Recurring tasks planner + calendar view
- [ ] v1.2 — SLA alerts + technician workload metrics
- [ ] v2.0 — Full statistics module + PDF/Excel exports

---

*Part of [ISTIC-QualityHub](../../README.md) — Back to suite / Retour à la suite*
