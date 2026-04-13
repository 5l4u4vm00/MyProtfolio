# Yi Hsuan Chao — Portfolio

**Live:** [arieschao.com](https://arieschao.com)

Full-stack developer portfolio built with Nuxt 4 + Vue 3, showcasing projects in Vue.js, Python, and .NET.

---

## Featured Projects

- **TaskFlow** — SaaS project management platform
- **Enterprise HR System** — Enterprise-grade HR and workforce platform
- **AI Document Assistant** — LLM-powered document processing tooling

---

## Tech Stack

| Category | Technologies |
|---|---|
| Frontend | Vue 3, Nuxt 4, TypeScript |
| Backend | Python (FastAPI), .NET |
| Database | PostgreSQL |
| Fonts | DM Sans, JetBrains Mono, Fraunces (Google Fonts) |

---

## Highlights

- Single-page SPA with smooth scroll navigation between sections
- Scroll-triggered reveal animations via Intersection Observer API
- Fully responsive layout with mobile menu
- Zero external UI library dependencies — custom CSS only

---

## Getting Started

```bash
npm install
npm run dev       # http://localhost:3000
npm run build     # production build
npm run preview   # preview production build
```

---

## Project Structure

```
app/
  pages/index.vue   # single-page portfolio (hero, projects, stack, about, blog, contact)
  app.vue           # root component
public/             # static assets (favicon, robots.txt)
nuxt.config.ts      # Nuxt config + Google Fonts
```
