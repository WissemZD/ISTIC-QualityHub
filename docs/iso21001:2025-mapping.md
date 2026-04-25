# 📐 ISO 21001:2018 — Clause Mapping

> Correspondance entre les applications ISTIC-QualityHub et les clauses ISO 21001:2018

---

## Overview / Vue d'ensemble

This document maps each application feature to the relevant clauses of ISO 21001:2018 (Educational Organizations Management System) and ISO 31000:2018 (Risk Management).

Ce document établit la correspondance entre chaque fonctionnalité des applications et les clauses pertinentes de l'ISO 21001:2018 (Système de management des organismes éducatifs) et l'ISO 31000:2018 (Management des risques).

---

## ISO 21001:2018 — Structure des clauses

| Clause | Title / Titre |
|---|---|
| **4** | Context of the organization — Contexte de l'organisme |
| 4.1 | Understanding the organization and its context |
| 4.2 | Understanding the needs and expectations of interested parties |
| 4.4 | EOMS and its processes |
| **5** | Leadership — Leadership |
| 5.1 | Leadership and commitment |
| 5.4 | Communication with learners and other beneficiaries |
| **6** | Planning — Planification |
| 6.1 | Actions to address risks and opportunities |
| 6.2 | EOMS objectives and planning to achieve them |
| **7** | Support — Support |
| 7.1 | Resources |
| 7.2 | Competence |
| 7.4 | Communication |
| 7.5 | Documented information |
| **8** | Operation — Réalisation des activités opérationnelles |
| 8.1 | Operational planning and control |
| 8.5 | Production and service provision |
| **9** | Performance evaluation — Évaluation des performances |
| 9.1 | Monitoring, measurement, analysis and evaluation |
| 9.3 | Management review |
| **10** | Improvement — Amélioration |
| 10.2 | Nonconformity and corrective action |

---

## Application → ISO Clause Mapping

### 🔴 Risk Manager

| Feature | ISO 21001:2018 | ISO 31000:2018 |
|---|---|---|
| Context analysis (internal/external issues) | §4.1 | §5.4.1 |
| Interested parties register | §4.2 | §5.4 |
| Risk identification | §6.1.1 | §6.3 |
| Risk assessment (V×G matrix) | §6.1.2 | §6.4 |
| Opportunity identification & assessment | §6.1.2 | §6.4 |
| Quality objectives linking | §6.2 | — |
| Action plans | §6.1.2, §6.2 | §6.5 |
| Responsible assignment | §7.1 | — |
| Stakeholder communication log | §5.4, §7.4 | §5.4 |
| Documented risk register | §7.5 | §6.7 |
| Monitoring & KPIs | §9.1 | §6.6 |
| Periodic review alerts | §9.1.3 | §6.6 |
| Audit trail / History | §7.5 | §6.7 |
| Management review report | §9.3 | — |
| Effectiveness evaluation | §10.2 | §6.6 |

### 🎫 Ticket Manager *(planned)*

| Feature | ISO 21001:2018 |
|---|---|
| Service request management | §8.1 |
| SLA compliance tracking | §9.1 |
| Resource / technician management | §7.1 |
| Recurring task planning | §8.5 |
| Statistics & trend analysis | §9.1.3 |
| Corrective actions | §10.2 |

### 🗓️ Leave Tracker *(planned)*

| Feature | ISO 21001:2018 |
|---|---|
| Staff directory | §7.1.2 |
| Training leave | §7.2 |
| Attendance monitoring | §9.1 |
| HR documented records | §7.5 |
| Absence trend reporting | §9.1.3 |

---

## SMOE — Processus de l'ISTIC

The following processes of ISTIC are supported by or mapped to ISTIC-QualityHub applications:

| Processus ISTIC | Application | Clause ISO 21001 |
|---|---|---|
| Gestion des risques institutionnels | Risk Manager | §6.1 |
| Support informatique & technique | Ticket Manager | §8.1, §9.1 |
| Gestion des ressources humaines | Leave Tracker | §7.1, §7.2 |
| Pilotage et indicateurs qualité | Process Dashboard *(planned)* | §9.1.3 |
| Audits internes | Audit Manager *(planned)* | §9.2 |
| Revue de direction | Risk Manager (§9.3 module) | §9.3 |

---

## Key Definitions / Définitions clés

**EOMS** — Educational Organization Management System (ISO 21001 terminology for the QMS in education context)

**SMOE** — Système de Management des Organismes d'Enseignement (terminologie française ISO 21001)

**Risk** / **Risque** — Effect of uncertainty on objectives (ISO 31000:2018, §3.1)

**Opportunity** / **Opportunité** — Positive effect of uncertainty — the upside of risk (ISO 31000:2018)

**Criticality** / **Criticité** — V×G (Vraisemblance × Gravité) = Likelihood × Severity score used for risk prioritization

---

*Part of [ISTIC-QualityHub](../README.md) — Back to root / Retour à la racine*
