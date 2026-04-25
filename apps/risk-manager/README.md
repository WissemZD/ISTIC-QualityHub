# 🔴 Risk Manager — Registre des Risques & Opportunités

> ISO 31000:2018 · ISO 21001:2018 · Standalone HTML Application

[![Version](https://img.shields.io/badge/Latest-v2.0-blue?style=flat-square)](#versions)
[![ISO 31000](https://img.shields.io/badge/ISO%2031000-2018-purple?style=flat-square)](https://www.iso.org/standard/65694.html)
[![ISO 21001](https://img.shields.io/badge/ISO%2021001-2018-blue?style=flat-square)](https://www.iso.org/standard/66266.html)
[![No Install](https://img.shields.io/badge/No%20Install-Open%20in%20Browser-green?style=flat-square)](#usage)

---

## 📋 Overview / Description

**EN** — A complete risk and opportunity management application for educational institutions, fully compliant with ISO 31000:2018 (Risk Management) and ISO 21001:2018 (Educational Organizations Management System). Designed as a single HTML file — no backend, no database, no installation required.

**FR** — Une application complète de gestion des risques et opportunités pour les établissements d'enseignement supérieur, entièrement conforme aux normes ISO 31000:2018 et ISO 21001:2018. Conçue en fichier HTML autonome — aucun backend, aucune base de données, aucune installation requise.

---

## ✨ Features / Fonctionnalités

### v2.0 (Latest / Actuelle)
- ✅ **Risk & Opportunity Register** — Full CRUD management with criticality scoring (V×G matrix)
- ✅ **Dynamic Action Plans** — Checklist-based tasks with automatic progress calculation
- ✅ **Periodic Review Alerts** — Dashboard alerts when a risk review is overdue (ISO 31000 §6.6)
- ✅ **Modification History** — Full audit trail per risk/opportunity
- ✅ **Stakeholder Communication** — Log which parties have been informed (ISO 31000 §5.4)
- ✅ **Quality Objectives Linking** — Relate risks to ISO 21001 §6.2 quality objectives
- ✅ **Management Review Report** — Auto-generated synthesis for §9.3 direction reviews
- ✅ **Custom Logo** — Upload institution logo displayed in header and PDF
- ✅ **Academic Cycle Filtering** — Filter dashboard by S1 / S2 / custom date range
- ✅ **KPI Dashboard** — C3 treatment rate, action completion rate, average closure delay
- ✅ **Export PDF** — Full landscape register with criticality color coding
- ✅ **Export Excel (XLSX)** — 4 sheets: Risks / Opportunities / Action Plan / KPIs
- ✅ **Export / Import JSON** — Backup and restore all data, share between devices

### v1.0
- ✅ Risk & Opportunity Register with V×G criticality matrix
- ✅ Action plan with manual progress slider
- ✅ PDF export
- ✅ Browser localStorage persistence

---

## 📐 ISO Mapping / Correspondance ISO

| Feature / Fonctionnalité | ISO 21001:2018 | ISO 31000:2018 |
|---|---|---|
| Risk identification & assessment | §6.1.2 | §6.4 |
| Opportunity management | §6.1.2 | §6.4 |
| Quality objectives linking | §6.2 | — |
| Action plans | §6.1.2, §6.2 | §6.5 |
| Stakeholder communication | §5.4, §7.4 | §5.4 |
| Monitoring & review | §9.1 | §6.6 |
| Management review | §9.3 | — |
| Audit trail / History | §7.5 | — |

---

## 📁 Versions

| Version | File | Release Date | Highlights |
|---|---|---|---|
| **v2.0** | [`v2.0/RiskManager_v2.html`](v2.0/RiskManager_v2.html) | 2025 | Full ISO suite, checklist, JSON export, logo, review |
| **v1.0** | [`v1.0/RiskManager_v1.html`](v1.0/RiskManager_v1.html) | 2025 | Initial release — standard risk register |

> 💡 **Recommendation** — Use **v2.0** for all new deployments. v1.0 is kept for reference only.

---

## 🚀 Usage / Utilisation

1. Download the latest version: [`v2.0/RiskManager_v2.html`](v2.0/RiskManager_v2.html)
2. Open in Chrome, Firefox, or Edge
3. Go to **Paramètres** → enter institution name, upload logo, configure processes and actors
4. Navigate to **Risques** or **Opportunités** to start registering
5. Use **Plan d'action** to create and track corrective actions
6. Monitor progress on the **Tableau de bord**
7. Generate reports from **Registre** (PDF / Excel) or **Revue direction** (PDF)

---

## 💾 Data Storage / Stockage des données

| Mechanism | Details |
|---|---|
| Storage | Browser `localStorage` — data stays in the browser on the local machine |
| Persistence | Survives page refresh and browser restart |
| Backup | Use **Export JSON** to save a `.json` file and **Import JSON** to restore |
| Sharing | Export JSON → share the file → colleague imports on their machine |
| Reset | Settings page → "Réinitialiser toutes les données" |

---

## 🗺️ Roadmap

- [ ] v2.1 — Logo displayed in PDF export header
- [ ] v2.2 — Multi-user mode via shared JSON file
- [ ] v2.3 — Email notification reminders for overdue reviews

---

## 🐛 Known Issues / Bugs connus

No known issues in v2.0. Report bugs via [GitHub Issues](../../issues).

---

*Part of [ISTIC-QualityHub](../../README.md) — Back to suite / Retour à la suite*
