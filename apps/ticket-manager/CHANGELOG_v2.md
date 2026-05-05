# 📋 Changelog — ISTIC-QualityHub

Tous les changements notables sont documentés ici.
All notable changes are documented here.

Format : [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
Versioning : [Semantic Versioning](https://semver.org/)

---

## [Unreleased] — En cours de développement

### 🎫 Ticket Manager v2.0 *(in development — ATOM by ATOM)*

#### 🔐 ATOM 1 — Design System + Auth Layer *(current)*
- SHA-256 password hashing via Web Crypto API (no external lib)
- Login screen with institution logo, username/password fields
- 3 roles: Admin / IT Technician / User with role-gated views
- Session management via sessionStorage with configurable timeout
- Login lockout after N failed attempts (ISO 27002 §8.5)
- Force password change on first login
- Inactivity auto-logout with overlay
- Sidebar user avatar + profile dropdown (change password, logout)

#### 🛡️ ATOM 2 — Admin Panel *(planned)*
- User account CRUD (create, edit, toggle active, reset password)
- Temporary password generation (one-time display)
- Watermark protection via admin password
- Session timeout & lockout configuration per institution

#### 🎟️ ATOM 3 — Tickets v2 *(planned)*
- Sequential numbering: TKT-2025-0001…
- Role-filtered views (user sees only own tickets)
- Ticket tags, related tickets, escalation workflow
- User satisfaction rating 1–5 ⭐ post-resolution
- Reopen counter for FCR metric

#### 📊 ATOM 4 — Dashboard & ISO Metrics *(planned)*
- MTTR, FCR, Reopen Rate, Satisfaction Score
- Heatmap: ticket creation by weekday × hour
- Period filter (Today / 7d / 30d / 90d / All)
- PDF monthly report (jsPDF + autoTable, lazy-loaded)

#### 📅 ATOM 5 — Recurring Tasks v2 *(planned)*
- Visual monthly calendar (7×6 CSS grid)
- Per-task execution checklist with steps
- Task dependencies (blocking)
- D-1 reminder notifications
- Compliance report: % on-time over 30d/90d

#### 🔔 ATOM 6 — Notifications v2 + Exports *(planned)*
- Typed, role-filtered notification center
- Excel multi-sheet export (SheetJS)
- PDF report with logo, KPIs, tickets table, tasks table

#### 🔧 ATOM 7 — Assembly + v1→v2 Migration *(planned)*
- Full file assembly with all ATOMs integrated
- v1 JSON auto-migration with field mapping
- Final JS syntax validation

---

## [1.0.0] — Ticket Manager v1.0 — 2025

### Added
- ✅ Full ticket CRUD with category, type, priority, service, description
- ✅ Workflow: New → In Progress → Resolved → Closed
- ✅ Dynamic SLA timers (Critical=4h, High=24h, Medium=48h, Low=72h)
- ✅ Visual SLA progress bar (green → orange → red → pulsing overdue)
- ✅ SLA auto-alerts at 80% elapsed and on breach (setInterval 60s)
- ✅ Ticket history log with notes, status changes, timestamps
- ✅ Ticket detail modal with contextual action buttons
- ✅ IT member management (CRUD) with avatar initials
- ✅ Dashboard: 5 KPI cards + status chart + priority chart + trend chart
- ✅ Technician workload bars
- ✅ Overdue SLA tickets table on dashboard
- ✅ Recurring tasks: CRUD, frequencies, mark done, auto next-due calc
- ✅ Task execution history log
- ✅ Internal audit log: CREATE/UPDATE/DELETE/LOGIN/EXPORT (max 500 entries)
- ✅ Input sanitization on all user fields (XSS prevention)
- ✅ Email validation via regex
- ✅ Content Security Policy meta tag
- ✅ Basic DevTools detection (log only, non-blocking)
- ✅ Logo upload (base64, persisted in localStorage)
- ✅ Dark / light mode toggle with persistence
- ✅ Dynamic watermark (institution name + current user)
- ✅ Export JSON (full data backup)
- ✅ Import JSON (full data restore with confirmation)
- ✅ Export CSV tickets (UTF-8 BOM, Excel-compatible)
- ✅ Toast notifications + notification panel with unread badge
- ✅ Simulated email via mailto: (ticket creation + assignment)
- ✅ Online/offline status indicator
- ✅ Keyboard shortcuts: N, Esc, D, T
- ✅ Legal footer with ISO 21001:2018 & ISO 27002:2022 mention
- ✅ Chart.js v4.4.3 via CDN with SRI integrity
- ✅ Fonts: Syne (display) + Outfit (body) + DM Mono (data)
- ✅ Reusable design system (CSS variables) for ISTIC-QualityHub suite

---

## [2.0.0] — Risk Manager v2 — 2025

### Added *(Risk Manager)*
- ✅ Custom institution logo upload (base64 in localStorage)
- ✅ Dynamic action checklist — sub-tasks with automatic progress %
- ✅ Periodic review date field per risk + dashboard alerts
- ✅ Modification history / audit trail per risk and opportunity
- ✅ Stakeholder communication log per risk (ISO 31000 §5.4)
- ✅ Quality objectives linking (ISO 21001 §6.2)
- ✅ Management review module §9.3 with PDF report
- ✅ Academic cycle filter (S1 / S2 / custom date range)
- ✅ KPI dashboard: C3 treatment rate, action completion, avg closure delay
- ✅ Excel export (XLSX, 4 sheets) via SheetJS CDN
- ✅ JSON export/import (full data backup/restore)
- ✅ Auto-status update based on checklist completion

### Fixed *(Risk Manager)*
- ✅ Template literal syntax error in `renderRevue()` — semicolon inside `${}` caused full JS crash

---

## [1.0.0] — Risk Manager v1 — 2025

### Added *(Risk Manager)*
- ✅ Risk register with V×G criticality matrix (C1/C2/C3)
- ✅ Opportunity register with Efforts×Advantage matrix (P1/P2/P3)
- ✅ Action plan with manual progress slider
- ✅ Process, actor, interested parties management
- ✅ Dashboard with distribution charts
- ✅ Effectiveness evaluation modal
- ✅ PDF export (jsPDF + AutoTable, landscape A4)
- ✅ Browser localStorage persistence

---

## Version Numbering / Numérotation

```
MAJOR.MINOR.PATCH

MAJOR → Refonte majeure ou nouvelle app dans la suite
MINOR → Nouvelle fonctionnalité (rétrocompatible)
PATCH → Correction de bug ou amélioration mineure

Exemples :
  1.0.0 → Première release
  1.1.0 → Nouvelle feature ajoutée
  2.0.0 → Refonte majeure (auth multi-rôles, etc.)
```

---

*Partie de [ISTIC-QualityHub](README.md)*
