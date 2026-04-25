# 🎓 ISTIC-QualityHub

> **Quality Management & Operations Suite for Higher Education**
> *Suite de gestion qualité et opérationnelle pour l'enseignement supérieur*

[![ISO 21001](https://img.shields.io/badge/ISO%2021001-2018-blue?style=flat-square)](https://www.iso.org/standard/66266.html)
[![ISO 31000](https://img.shields.io/badge/ISO%2031000-2018-purple?style=flat-square)](https://www.iso.org/standard/65694.html)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Apps](https://img.shields.io/badge/Apps-1%20released-orange?style=flat-square)](#applications)
[![Institution](https://img.shields.io/badge/ISTIC-Université%20de%20Carthage-red?style=flat-square)](https://www.ucar.tn)

---

## 🏛️ About / À propos

**EN** — ISTIC-QualityHub is an open-source suite of standalone HTML applications designed to support the quality management system of [ISTIC (Institut Supérieur des Technologies de l'Information et de la Communication)](https://www.istic.rnu.tn), University of Carthage, Tunisia. Each application is a single self-contained HTML file — no server, no database, no installation required.

**FR** — ISTIC-QualityHub est une suite d'applications HTML autonomes conçue pour soutenir le système de management de la qualité de l'[ISTIC (Institut Supérieur des Technologies de l'Information et de la Communication)](https://www.istic.rnu.tn), Université de Carthage, Tunisie. Chaque application est un fichier HTML autonome — aucun serveur, aucune base de données, aucune installation requise.

---

## 🌐 Standards Compliance / Conformité normative

| Standard | Scope / Périmètre |
|---|---|
| **ISO 21001:2018** | Educational Organizations Management System — Système de management des organismes d'enseignement |
| **ISO 31000:2018** | Risk Management — Management des risques |
| **ISO 9001:2015** | Quality Management Systems — Principes généraux qualité |

---

## 📦 Applications

| App | Version | Description | Status |
|---|---|---|---|
| 🔴 [Risk Manager](apps/risk-manager/) | v2.0 | Risk & opportunity register — Registre des risques & opportunités | ✅ Released |
| 🎫 [Ticket Manager](apps/ticket-manager/) | v1.0 | IT & technical support tickets — Tickets d'intervention | 🚧 In progress |
| 🗓️ [Leave Tracker](apps/leave-tracker/) | v1.0 | Staff attendance & leave management — Congés & présence | 📋 Planned |
| 📊 [Process Dashboard](apps/process-dashboard/) | v1.0 | Quality KPIs by process — Indicateurs qualité par processus | 📋 Planned |
| 📋 [Audit Manager](apps/audit-manager/) | v1.0 | Internal audit planning — Planification des audits internes | 📋 Planned |

---

## 🗂️ Repository Structure / Structure du dépôt

```
ISTIC-QualityHub/
│
├── README.md                        ← You are here / Vous êtes ici
├── CHANGELOG.md                     ← Version history / Historique des versions
├── LICENSE                          ← MIT License
│
├── apps/                            ← All applications / Toutes les applications
│   ├── risk-manager/
│   │   ├── README.md
│   │   ├── v1.0/
│   │   │   └── RiskManager_v1.html
│   │   └── v2.0/
│   │       └── RiskManager_v2.html
│   │
│   ├── ticket-manager/
│   │   └── README.md
│   │
│   └── leave-tracker/
│       └── README.md
│
├── docs/                            ← General documentation / Documentation générale
│   ├── architecture.md              ← Technical architecture / Architecture technique
│   └── iso21001-mapping.md          ← ISO 21001 clause mapping / Correspondance clauses
│
└── .github/
    └── ISSUE_TEMPLATE/              ← Bug report templates / Modèles de signalement
```

---

## 🚀 How to use / Comment utiliser

**EN**
1. Navigate to the desired application folder (e.g. `apps/risk-manager/v2.0/`)
2. Download the `.html` file
3. Open it in any modern browser (Chrome, Firefox, Edge)
4. Data is saved automatically in your browser's local storage
5. Use **Export JSON** to back up your data or share between devices

**FR**
1. Naviguez vers le dossier de l'application souhaitée (ex. `apps/risk-manager/v2.0/`)
2. Téléchargez le fichier `.html`
3. Ouvrez-le dans n'importe quel navigateur moderne (Chrome, Firefox, Edge)
4. Les données sont sauvegardées automatiquement dans le stockage local du navigateur
5. Utilisez **Exporter JSON** pour sauvegarder vos données ou les partager entre appareils

> ⚠️ **Important** — Data is stored locally in your browser. Clearing browser cache will erase all data. Always export a JSON backup regularly. / Les données sont stockées localement dans votre navigateur. Vider le cache effacera toutes les données. Exportez régulièrement une sauvegarde JSON.

---

## 🤝 Contributing / Contribuer

Contributions, bug reports and feature requests are welcome.
Les contributions, signalements de bugs et demandes de fonctionnalités sont les bienvenues.

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-new-feature`
3. Commit your changes: `git commit -m "feat: add my new feature"`
4. Push to the branch: `git push origin feature/my-new-feature`
5. Open a Pull Request

---

## 📄 License

MIT License — © 2025 ISTIC, Université de Carthage, Tunisia.
See [LICENSE](LICENSE) for details.

---

## 👨‍💻 Maintainer / Mainteneur

**ISTIC — Institut Supérieur des Technologies de l'Information et de la Communication**
Université de Carthage — Tunisie
🌐 [www.istic.rnu.tn](https://www.istic.rnu.tn) | 🌐 [www.ucar.tn](https://www.ucar.tn)

---

*Built with ❤️ for quality-driven education — Construit avec ❤️ pour une éducation axée sur la qualité*
------------------------------ Wissem Zeddini ----------------------------------------------------
