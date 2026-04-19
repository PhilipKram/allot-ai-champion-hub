# Allot AI Champion Hub

Self-contained training hub for the Allot AI Champion Enablement Program — pre-work, 2-day workshop agenda, readiness exam, and completion checklist.

Live site: _add GitHub Pages URL after setup_

## What's here

| File | Purpose |
|---|---|
| `index.html` | The hub itself. Single-file site with 5 tabs (Home, Pre-Work, Workshop, Exam, Checklist). Served as the GitHub Pages root. |
| `AI_Champion_Hub.html` | Identical copy of `index.html`. Kept so the canonical filename is obvious when browsing the repo. |
| `AI_Champion_Pre-Work.md` | Source doc for pre-work content. Canonical text; the hub mirrors this. |
| `AI_Champion_Enablement_Training.md` | Source doc for the 2-day workshop agenda. |
| `AI_Champion_Readiness_Exam.html` | Standalone offline version of the exam (kept as backup; the hub has the same exam embedded). |
| `AI_Champion_Pre-Work.html` / `AI_Champion_Enablement_Training.html` | Earlier standalone HTML exports. Superseded by the hub; kept for reference. |
| `AI_Champion_Validation_Brief.md` | Internal validation brief for the program. |
| `AI_Tools_License_Request.xlsx` | License request spreadsheet. |

## Audience

Champions across Allot R&D, Product, Security, and Support. Multi-region cohort: IL (in-person, Hod HaSharon) + remote EU and India.

## Program shape

- **Pre-Work** — 4 hours self-paced. Readiness Exam submitted 48h before Day 1.
- **Workshop** — 2 days, 10:00–18:00 IL, hybrid.
- **Post-Training** — 90-day roadmap. First local workshop within 2 weeks.

## Editing

The source of truth for content is the Markdown files. When you update the Markdown, also update the matching panels in `index.html` (and `AI_Champion_Hub.html`) to keep the hub in sync.

## Local preview

Open `index.html` in a browser. The hub stores exam and checklist progress in the browser's `localStorage` (stays on the user's device; nothing is sent to a server).

## Deployment

GitHub Pages serves `index.html` from the repo root. Settings → Pages → Source: `main` branch / root.

---

© Allot Ltd. — AI Enablement & Standards — 2026
