# RDHS Statistics Dashboard (PWA)

A modern, responsive, offline-capable **Progressive Web Application** built for the **Regional Director of Health Services (RDHS), Trincomalee** — providing interactive visualisation and monitoring of district-level public health statistics.

🌐 **Live:** [https://jeevantjr.github.io/rdhs-stats-pwa/](https://jeevantjr.github.io/rdhs-stats-pwa/)

---

## Features

- **Progressive Web App** — installable on mobile and desktop with full offline support via service worker and pre-cached routes
- **Health Statistics Dashboards** — dynamic charts and clean tabular views powered by Chart.js; covers dengue, bed occupancy, outdoor/indoor patients, maternal deaths, and more
- **MOH & Hospital Cadre Data** — workforce distribution by cadre, institution, and MOH division with downloadable PDF summaries
- **Clinic & Outpatient Schedules** — hospital and PMCU schedules across Trincomalee district
- **Monthly Statistics** — focused dengue monitoring and outbreak tracking views
- **Health Education Materials** — preventive health resources including infant feeding guidance
- **Downloadable Reports** — health service summaries and cadre PDFs
- **Lightweight & Fast** — Bootstrap 4 layout, optimised for low-bandwidth environments

---

## Navigation

| Section | Contents |
|---|---|
| Dashboard | District-wide health service overview |
| Card Details | MOH cadre · Hospital cadre · Summary PDFs |
| Statistics | Communicable diseases · Maternal deaths · Health personnel · Births · Hospital beds & admissions · Dengue |
| Institutions | Outpatient schedules · Special clinics |
| Health Education | Baby feeding · Additional modules |
| Monthly Statistics | Dengue stats · Outbreak monitoring |

---

## Tech Stack

- **HTML5 · CSS3 · JavaScript (Vanilla)**
- **Chart.js** — interactive graphs
- **Bootstrap 4** — responsive layout
- **Service Worker + Web App Manifest** — PWA capabilities
- **GitHub Pages** — hosting

---

## PWA Capabilities

- **Offline access** — all major pages pre-cached; works with limited or no connectivity
- **Add to Home Screen** — installable on Android, iOS, and desktop
- **Auto-caching** — key assets cached on first load for instant subsequent access

---

## Local Development

```bash
git clone https://github.com/jeevantjr/rdhs-stats-pwa.git
cd rdhs-stats-pwa
# Open index.html in your browser, or serve locally:

python -m http.server 8000
# or
npx serve .
```

---

## Developer

**Dr. Thangarasa Jeevaraaj**
MBBS · MCGP · MSc Biomedical Informatics (PGIM, Batch 12)
MD Health Informatics Trainee — Batch 9, PGIM, University of Colombo

This project was built during a posting as Medical Officer (Health Information) at the RDHS Office, Trincomalee, as part of a broader effort to bring data-driven tools to district public health administration in Sri Lanka.

- 🌐 Website: [drjeevaraj.com](https://drjeevaraj.com)
- 💻 GitHub: [github.com/jeevantjr](https://github.com/jeevantjr)
- 🔬 AI Reviewer Profile: [drjeevaraj.com/ai-reviewer](https://drjeevaraj.com/ai-reviewer.html)

---

## Feedback & Collaboration

Issues and pull requests are welcome. For collaboration inquiries, open a GitHub Issue or contact via the website.

---

## License

[MIT License](https://opensource.org/licenses/MIT)
