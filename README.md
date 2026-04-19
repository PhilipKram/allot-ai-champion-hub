# Allot AI Champion Hub

Self-contained training hub for the Allot AI Champion Enablement Program — pre-work, 2-day workshop agenda, and post-training certification exam.

**Live site:** https://philipkram.github.io/allot-ai-champion-hub/

**2026 Q2 Cohort:** Day 1 — Wed 29 Apr 2026 · Day 2 — Mon 4 May 2026 · 10:00–18:00 IL · hybrid (in-person Hod HaSharon + remote EU/India via Teams)

## What's here

| File | Purpose |
|---|---|
| `index.html` | The hub itself. Single-file site with 4 tabs (Home, Pre-Work, Workshop, Certification Exam). Served as the GitHub Pages root. |
| `AI_Champion_Hub.html` | Identical copy of `index.html`. Kept so the canonical filename is obvious when browsing the repo. |
| `AI_Champion_Pre-Work.md` | Source doc for pre-work content. Canonical text; the hub mirrors this. |
| `AI_Champion_Enablement_Training.md` | Source doc for the 2-day workshop agenda. |
| `AI_Champion_Pre-Work.html` / `AI_Champion_Enablement_Training.html` | Earlier standalone HTML exports. Superseded by the hub; kept for reference. |
| `AI_Champion_Validation_Brief.md` | Internal validation brief for the program. |
| `AI_Tools_License_Request.xlsx` | License request spreadsheet. |

## Audience

Champions across Allot R&D, Product, Security, and Support. Multi-region cohort: IL (in-person, Hod HaSharon) + remote EU and India.

## Program shape

- **Pre-Work** — 2.5 hours self-paced. No gating exam; per-part completion checkboxes.
- **Workshop** — 2 days, 10:00–18:00 IL, hybrid.
- **Certification Exam** — post-training, submitted within 7 days of Day 2.
- **Post-Training** — 30-day roadmap. First local workshop within 2 weeks.

## Editing

The source of truth for content is the Markdown files. When you update the Markdown, also update the matching panels in `index.html` (and `AI_Champion_Hub.html`) to keep the hub in sync.

## Local preview

Open `index.html` in a browser. The hub stores exam and checklist progress in the browser's `localStorage` (stays on the user's device; nothing is sent to a server).

## Deployment

GitHub Pages serves `index.html` from the repo root. Settings → Pages → Source: `main` branch / root.

---

© Allot Ltd. — AI Enablement & Standards — 2026
