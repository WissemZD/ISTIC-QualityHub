# 🏗️ Technical Architecture — Architecture Technique

> ISTIC-QualityHub · Technical Design Document

---

## Design Philosophy / Philosophie de conception

**EN** — Every application in ISTIC-QualityHub follows the same core principle: **zero infrastructure**. No server, no database, no framework, no build step. A user downloads one `.html` file, opens it in a browser, and has a fully functional application. This choice is deliberate — it maximizes accessibility in institutional environments where IT constraints, network restrictions, or budget limitations make server-based solutions impractical.

**FR** — Chaque application d'ISTIC-QualityHub suit le même principe fondamental : **zéro infrastructure**. Aucun serveur, aucune base de données, aucun framework, aucune étape de compilation. Un utilisateur télécharge un fichier `.html`, l'ouvre dans un navigateur, et dispose d'une application entièrement fonctionnelle. Ce choix est délibéré — il maximise l'accessibilité dans les environnements institutionnels où les contraintes informatiques, les restrictions réseau ou les limites budgétaires rendent les solutions serveur peu pratiques.

---

## Architecture Pattern

```
┌─────────────────────────────────────────────────────┐
│                  Single HTML File                    │
│                                                      │
│  ┌──────────┐  ┌──────────────┐  ┌───────────────┐  │
│  │   CSS    │  │     HTML     │  │  JavaScript   │  │
│  │ (styles) │  │  (structure) │  │   (logic)     │  │
│  └──────────┘  └──────────────┘  └───────────────┘  │
│                                         │            │
│                              ┌──────────▼──────────┐ │
│                              │   State Object (S)  │ │
│                              │  { risques: [],     │ │
│                              │    actions: [],     │ │
│                              │    actors: [], … }  │ │
│                              └──────────┬──────────┘ │
│                                         │            │
│                              ┌──────────▼──────────┐ │
│                              │   localStorage      │ │
│                              │  (browser storage)  │ │
│                              └─────────────────────┘ │
└─────────────────────────────────────────────────────┘
```

---

## Data Flow / Flux de données

```
User Action (click/input)
        │
        ▼
  Event Handler (JS function)
        │
        ▼
  Update State Object S
        │
        ├──► save() → localStorage.setItem()   [persist]
        │
        └──► render*() → DOM update            [display]


Page Load:
  load() → localStorage.getItem() → Object.assign(S, data) → renderAll()
```

---

## Storage Strategy / Stratégie de stockage

| Mechanism | Scope | Lifetime | Size limit |
|---|---|---|---|
| `localStorage` | Per browser per machine | Until manually cleared | ~5-10 MB |
| JSON Export | Portable file | Permanent | Unlimited |
| JSON Import | Restore from file | One-time operation | N/A |

### Storage Key Convention
Each app uses a unique key to avoid conflicts:
```javascript
// risk-manager
const DB = 'rmapp-v2-iso';

// ticket-manager (planned)
const DB = 'ticketapp-v1-istic';

// leave-tracker (planned)
const DB = 'leaveapp-v1-istic';
```

---

## External Dependencies / Dépendances externes

All libraries are loaded from CDN **on demand** (only when needed for export):

| Library | Version | Usage | CDN |
|---|---|---|---|
| [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 | PDF generation | cdnjs |
| [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable) | 3.8.2 | PDF tables | cdnjs |
| [SheetJS (XLSX)](https://sheetjs.com/) | 0.18.5 | Excel export | cdnjs |
| [Google Fonts](https://fonts.google.com/) | — | Typography (DM Sans, DM Serif Display) | Google |

> ⚠️ **Offline use** — Applications require internet access only for PDF/Excel export (CDN libraries) and font loading. Core functionality works offline if fonts are cached.

---

## Coding Conventions / Conventions de code

### JavaScript
```javascript
// State object — single source of truth
let S = { /* all app data */ };

// Naming: render* for DOM updates, save* for persistence
function renderRisques() { /* update DOM */ }
function saveRisque()    { /* update S + call save() */ }
function save()          { localStorage.setItem(DB, JSON.stringify(S)); }
function load()          { Object.assign(S, JSON.parse(localStorage.getItem(DB))); }

// Unique IDs
function uid() { return Date.now().toString(36) + Math.random().toString(36).slice(2,5); }
```

### CSS
```css
/* CSS variables for theming — always use variables, never hardcode colors */
:root {
  --blue: #1a3fa0;
  --purple: #5c2fc5;
  --green: #12a05a;
  /* etc. */
}
```

### Template Literals — Important Rule
When using dynamic values inside HTML `style=""` attributes within template literals:
```javascript
// ✅ CORRECT — closing } before semicolon
`<span style="color:${condition ? 'red' : 'green'};font-weight:700">`

// ❌ WRONG — semicolon inside ${ } breaks JS parser
`<span style="color:${condition ? 'red' : 'green';font-weight:700}">`
```

---

## File Naming Convention / Convention de nommage des fichiers

```
AppName_vMAJOR.MINOR.html

Examples:
  RiskManager_v1.html          ← Major version 1, no sub-version
  RiskManager_v2.html          ← Major version 2
  TicketManager_v1.html
  LeaveTracker_v1.html
```

---

## Browser Compatibility / Compatibilité navigateur

| Browser | Support |
|---|---|
| Chrome / Chromium 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Internet Explorer | ❌ Not supported |

---

*Part of [ISTIC-QualityHub](../README.md) — Back to root / Retour à la racine*
