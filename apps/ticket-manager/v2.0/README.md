# 🎫 Ticket Manager — Gestion des Demandes d'Intervention IT & Technique

> IT & Technical Support · ISO 21001:2025 · ISO 27002:2022 · Standalone HTML Application

[![v1.0 Released](https://img.shields.io/badge/v1.0-Released-green?style=flat-square)](#versions)
[![v2.0 In Dev](https://img.shields.io/badge/v2.0-In%20Development-orange?style=flat-square)](#versions)
[![ISO 21001](https://img.shields.io/badge/ISO%2021001-2025-blue?style=flat-square)](https://www.iso.org/standard/66266.html)
[![ISO 27002](https://img.shields.io/badge/ISO%2027002-2022-purple?style=flat-square)](https://www.iso.org/standard/75652.html)
[![No Install](https://img.shields.io/badge/No%20Install-Open%20in%20Browser-green?style=flat-square)](#usage)

---

## 📋 Overview / Description

**EN** — A complete IT & technical support ticketing system designed for higher education institutions. Manage intervention requests, track SLA compliance, monitor technician workloads, plan recurring tasks, and generate statistics dashboards — all in a single standalone HTML file with no server, no database, no installation.

**FR** — Un système de tickets complet pour le support informatique et technique des établissements d'enseignement supérieur. Gérez les demandes d'intervention, suivez la conformité SLA, surveillez la charge des techniciens, planifiez les tâches récurrentes et générez des tableaux de bord statistiques — tout dans un seul fichier HTML autonome, sans serveur, sans base de données, sans installation.

---

## 🎯 Target Processes / Processus ciblés

- 🖥️ IT infrastructure support (hardware, network, servers)
- 💻 Software support (installations, licenses, configurations)
- 🔧 Technical maintenance (equipment, facilities)
- 🔒 Security incidents
- 📋 Recurring scheduled tasks (backups, updates, maintenance)
- 🏗️ *(v3)* Project & contractor follow-up — Suivi projets prestataires

---

## ✨ Features by Version / Fonctionnalités par version

### ✅ v1.0 — Released (Standalone, no auth)

#### Ticket Management
- [x] Create tickets: category, priority, type, affected service, description
- [x] Workflow: New → In Progress → Resolved → Closed
- [x] Dynamic assignment from configured IT team members
- [x] SLA timers per priority (Critical=4h, High=24h, Medium=48h, Low=72h)
- [x] Visual SLA progress bar with color coding (green → orange → red)
- [x] Notes & resolution history per ticket with timestamps
- [x] Ticket detail modal with full action history

#### Dashboard & Metrics
- [x] Real-time KPI stats: open / in-progress / resolved / closed / overdue
- [x] SLA compliance rate (%)
- [x] Doughnut charts: tickets by status & priority (Chart.js)
- [x] Monthly trend chart: created vs resolved (12 months)
- [x] Technician workload bars
- [x] Overdue SLA tickets list with elapsed time

#### Planning — Recurring Tasks
- [x] Define recurring tasks (daily / weekly / monthly / quarterly)
- [x] Mark task as executed → auto-calculate next due date
- [x] Execution history log
- [x] Overdue & upcoming task alerts

#### Security & Compliance (ISO 27002:2022)
- [x] Input sanitization on all user-facing fields
- [x] Email validation via regex
- [x] Internal audit log (CREATE / UPDATE / DELETE / LOGIN / EXPORT)
- [x] Content Security Policy meta tag
- [x] Basic DevTools detection (log only)
- [x] Generic error messages (no stack trace exposure)

#### Settings & UX
- [x] Logo upload (base64, persisted in localStorage)
- [x] Institution name, current user, SLA configuration
- [x] IT team member management (CRUD)
- [x] Dark / light mode toggle (persisted)
- [x] Dynamic watermark (toggleable, shows institution + user)
- [x] Export JSON (full backup) / Import JSON (restore)
- [x] Export CSV tickets (UTF-8 BOM, Excel-compatible)
- [x] Keyboard shortcuts: N=new ticket, Esc=close, D=dashboard, T=tickets
- [x] Toast notifications + notification panel
- [x] Simulated email via mailto: with pre-filled subject & body
- [x] Online/offline status indicator
- [x] Legal footer (ISO compliance, copyright)

---

### 🚧 v2.0 — In Development (Multi-role auth)

#### Authentication & Access Control (ISO 27002 §5.15, §5.16)
- [ ] Login screen with username + password (SHA-256 via Web Crypto API)
- [ ] 3 roles: **Admin** / **IT Technician** / **User (Requester)**
- [ ] Session management in sessionStorage (auto-expires)
- [ ] Inactivity timeout (configurable: 15/30/60/120 min)
- [ ] Login lockout after N failed attempts (configurable: 3/5/10)
- [ ] Force password change on first login
- [ ] Session expired overlay

#### Role-Based Views
- [ ] **Admin** → full access: all tickets, all metrics, user management, settings
- [ ] **IT Technician** → assigned tickets + unassigned pool, planning, personal dashboard
- [ ] **User** → create tickets, track own tickets only, rate resolved tickets

#### Ticket Enhancements v2
- [ ] Sequential ticket numbering: TKT-2025-0001, TKT-2025-0002…
- [ ] Ticket tags (chips, max 5, filterable)
- [ ] Related tickets linking (bidirectional)
- [ ] Escalation: IT → Admin with reason modal + escalation badge
- [ ] User satisfaction rating 1–5 ⭐ after ticket resolved
- [ ] Reopen counter (tracked for FCR metric)
- [ ] Simplified creation form for User role (no priority/assignment fields)
- [ ] Step-by-step progression visual for User "My Tickets" view

#### Dashboard & Metrics v2 (ISO 21001:2025 §9.1.3)
- [ ] MTTR (Mean Time To Resolve) by category & technician
- [ ] FCR (First Contact Resolution Rate)
- [ ] Reopen Rate
- [ ] Average satisfaction score (global + per technician)
- [ ] Creation heatmap (weekday × hour grid)
- [ ] Period filter: Today / 7d / 30d / 90d / All
- [ ] Role-adapted dashboard (admin=global, IT=personal, user=simplified)

#### Recurring Tasks v2
- [ ] Visual monthly calendar (7×6 grid, color-coded by task status)
- [ ] Per-task execution checklist (steps with done/undone + timestamp)
- [ ] Task dependencies (task B blocked until task A complete)
- [ ] D-1 reminder notifications
- [ ] Task compliance report: % executed on time over 30d/90d

#### Exports v2
- [ ] PDF monthly report (jsPDF + autoTable, lazy-loaded): KPIs + tickets + tasks
- [ ] Excel multi-sheet export (SheetJS): Tickets / Metrics / Tasks / Audit / Members
- [ ] Institution logo embedded in PDF header

#### Notifications v2
- [ ] Typed notifications: sla_warn, ticket_assigned, escalation, task_due, rating_request…
- [ ] Notification center with tabs: All / Unread / Tickets / Tasks / System
- [ ] Grouped by date (Today / Yesterday / Older)
- [ ] Configurable SLA reminders: at 50%, 75%, 90% elapsed
- [ ] Role-filtered notifications (each role receives only relevant alerts)

#### Admin Panel v2
- [ ] User account CRUD (username, displayName, email, role, department)
- [ ] Toggle account active/inactive
- [ ] Password reset with one-time temporary password display
- [ ] Watermark protection via admin password
- [ ] Session timeout & lockout configuration

#### Migration
- [ ] Import v1 JSON → auto-mapped to v2 schema with defaults

---

### 📋 v3.0 — Planned (Backend + Contractor Management)

> Requires a backend server (Node.js / PHP + SQLite) and separate role files

#### Contractor & Project Follow-up
- [ ] Contractor registry (company, contact, contract reference)
- [ ] Project tracking: milestones, deliverables, deadlines
- [ ] Provisional receipt (PV réception provisoire) — upload + digital signature
- [ ] Final receipt (PV réception définitive) — upload + digital signature
- [ ] Compliance gap tracking between provisional and final reception

#### IT Procurement Management
- [ ] Equipment needs definition form (department → IT review → approval)
- [ ] Purchase validation workflow: Request → Quote → Order → Reception → Compliance check
- [ ] Technical conformity checklist per purchase category
- [ ] Asset inventory link

#### Architecture v3
- [ ] Separate files: `admin.html` / `it.html` / `user.html`
- [ ] REST API backend (Node.js / PHP)
- [ ] SQLite or PostgreSQL database
- [ ] JWT authentication
- [ ] Email notifications (real SMTP, not mailto:)
- [ ] Role-based API endpoints

---

## 📐 ISO Mapping / Correspondance normative

### ISO 21001:2025

| Feature / Fonctionnalité | Clause ISO 21001:2025 |
|---|---|
| Ticket = service request management | §8.1 — Operational planning & control |
| SLA tracking & compliance | §9.1 — Monitoring & measurement |
| Technician resource & workload | §7.1 — Resources |
| Recurring task planning | §8.5 — Production & service provision |
| Dashboard KPIs & trends | §9.1.3 — Analysis & evaluation |
| MTTR, FCR, satisfaction metrics | §9.1.3 — Performance indicators |
| PDF monthly report | §9.1.3 — Reporting evidence |
| Management review data feed | §9.3 — Management review |
| Corrective actions (escalation) | §10.2 — Nonconformity & corrective action |

### ISO 27002:2022

| Feature / Fonctionnalité | Clause ISO 27002:2022 |
|---|---|
| Authentication + SHA-256 | §5.16 — Identity management |
| Role-based access control | §5.15 — Access control |
| Session timeout & lockout | §8.5 — Secure authentication |
| Input sanitization | §8.28 — Secure coding |
| Internal audit log | §8.15 — Logging |
| Data export controls | §5.12 — Classification |
| CSP meta tag | §8.20 — Network security |
| Watermark & copyright | §5.32 — Intellectual property |

---

## 📁 Versions / Fichiers

| Version | Fichier | Statut | Points clés |
|---|---|---|---|
| **v1.0** | [`v1.0/TicketManager_v1.html`](v1.0/TicketManager_v1.html) | ✅ Released | Single user, full ticketing, SLA, planning, audit |
| **v2.0** | `v2.0/TicketManager_v2.html` | 🚧 In development | Multi-role auth, metrics ISO, calendar, PDF/Excel |
| **v3.0** | `v3.0/` *(dossier)* | 📋 Planned | Backend, contractors, procurement |

> 💡 **Pour un déploiement immédiat** → utiliser **v1.0**. Elle est complète et fonctionnelle.
> 💡 **For immediate deployment** → use **v1.0**. It is complete and fully functional.

---

## 🚀 Usage / Utilisation (v1.0)

1. Télécharger [`v1.0/TicketManager_v1.html`](v1.0/TicketManager_v1.html)
2. Ouvrir dans Chrome, Firefox ou Edge (v90+)
3. Aller dans **Paramètres** → configurer établissement, logo, membres IT
4. Créer des tickets via le bouton **"Nouveau ticket"** ou la touche `N`
5. Les données sont sauvegardées automatiquement dans le `localStorage`
6. Exporter régulièrement : **Paramètres → Exporter JSON**

---

## 💾 Data & Storage

| Aspect | Détail |
|---|---|
| Stockage | `localStorage` — données locales au navigateur/machine |
| Session (v2) | `sessionStorage` — token de session, disparaît à fermeture |
| Backup | Export JSON → partager le fichier → Import JSON sur autre machine |
| Reset | Paramètres → "Réinitialiser toutes les données" |

---

## 🗺️ Development Roadmap

```
2026 Q1-Q2   v1.0  ✅  Core ticketing + SLA + planning + audit
2026 Q2-Q3   v2.0  🚧  Multi-role auth + metrics ISO + calendar + PDF/Excel
2026 Q4      v3.0  📋  Backend + contractors + procurement
```

---

## 🐛 Issues & Contributions

Signaler un bug ou proposer une amélioration → [GitHub Issues](../../issues)

---

*Partie de [ISTIC-QualityHub](../../README.md) — Retour à la suite / Back to suite*

