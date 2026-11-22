# Norbert Aguilera - Portfolio (Google Style)

Personal portfolio built with **Next.js 15 (App Router)**, **TypeScript**, **Tailwind CSS 4** and **React 19**, styled like Google search results.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FNorbertAguilera%2Fporfoleo_google)

Actual deployment: [porfoleo-norbertaguilera.vercel.app/es](https://porfoleo-norbertaguilera.vercel.app/es)

---

## 🚀 Quick Start

```bash
npm install
npm run dev      # http://localhost:3000
npm run build
npm start
```

Alternatively, with Docker (from the repository root):

```bash
cd mi-portfolio
docker-compose up --build
```

---

## 📁 Project Structure

```
mi-portfolio/
├── app/
│   ├── [lang]/                 # i18n routes: es, en, ca
│   │   ├── page.tsx            # Home: search results + knowledge panel
│   │   ├── IA/page.tsx         # AI Overview style page
│   │   ├── projects/page.tsx   # Projects showcase
│   │   └── tecnologies/page.tsx # Technologies with category filters
│   ├── globals.css             # Tailwind + CSS variables (dark mode ready)
│   └── layout.tsx              # Root layout + Header
├── components/
│   ├── Header.tsx              # Google-style header, search bar, nav
│   ├── TechGrid.tsx            # Filterable technology badges
│   └── langSwitcher.tsx        # ES / EN / CA switcher
├── lib/
│   └── dictonary.ts            # Dictionary loader
├── dictonaries/
│   ├── es.json
│   ├── en.json
│   └── ca.json
├── public/
│   ├── images/                 # Project screenshots
│   └── Curiculums/             # CV PDFs (ES, EN, CA)
└── next.config.ts
```

> Note: the folder is actually named `dictonaries` (typo in the repo), not `dictionaries`.

---

## ✅ Implemented

| Feature | Status | Notes |
|---------|--------|-------|
| Home page | ✅ | Google results layout + knowledge panel |
| Projects | ✅ | 6 projects with screenshots, stack and GitHub links |
| Technologies | ✅ | 37 technologies, category tabs |
| IA page | ✅ | AI Overview style, experience and skills |
| i18n | ✅ | ES / EN / CA via route param and dictionaries |
| Header / nav | ✅ | Search bar, tabs, language switcher |
| CVs | ✅ | 3 PDFs in `public/Curiculums/` |
| Project images | ✅ | Screenshots in `public/images/` |
| Responsive | ✅ | Mobile-first, md/lg breakpoints |
| Dark mode | ⚠️ | CSS variables only, no UI toggle yet (issue #14) |

---

## 🚧 Roadmap (GitHub issues)

Full list: [github.com/NorbertAguilera/porfoleo_google/issues](https://github.com/NorbertAguilera/porfoleo_google/issues)

### 🔴 Phase 1 — missing pages (header links currently 404)

| Issue | Page | Description | Effort |
|-------|------|-------------|--------|
| [#2](https://github.com/NorbertAguilera/porfoleo_google/issues/2) | `/about` | Expanded bio, values, soft skills, photo, timeline | Medium |
| [#3](https://github.com/NorbertAguilera/porfoleo_google/issues/3) | `/experience` | Work history: companies, roles, dates, achievements, tech | Medium |
| [#4](https://github.com/NorbertAguilera/porfoleo_google/issues/4) | `/contact` | Contact form, social links, booking link, validation + toasts | Medium |
| [#5](https://github.com/NorbertAguilera/porfoleo_google/issues/5) | `/blog` | Article list (external links or local MDX) | Low-Medium |

### 🟡 Phase 2 — SEO and technical foundation

| Issue | Feature | Description | Effort |
|-------|---------|-------------|--------|
| [#6](https://github.com/NorbertAguilera/porfoleo_google/issues/6) | Per-page metadata | Unique title, description, OG/Twitter tags, hreflang | Low |
| [#7](https://github.com/NorbertAguilera/porfoleo_google/issues/7) | `sitemap.xml` | Auto-generated, all locales | Low |
| [#8](https://github.com/NorbertAguilera/porfoleo_google/issues/8) | `robots.txt` | Crawler allow/disallow rules | Low |
| [#9](https://github.com/NorbertAguilera/porfoleo_google/issues/9) | Custom 404 | "No results found" page with links home | Low |
| [#10](https://github.com/NorbertAguilera/porfoleo_google/issues/10) | JSON-LD | Person, WebSite, BreadcrumbList, Project schemas | Medium |
| [#11](https://github.com/NorbertAguilera/porfoleo_google/issues/11) | Favicon set | PNG sizes, Apple touch, manifest, Safari mask | Low |

### 🟢 Phase 3 — content and UX

| Issue | Feature | Description | Effort |
|-------|---------|-------------|--------|
| [#12](https://github.com/NorbertAguilera/porfoleo_google/issues/12) | Profile photo | Real portrait in the knowledge panel | Low |
| [#13](https://github.com/NorbertAguilera/porfoleo_google/issues/13) | Panel images | Fill the 4 image slots on the home page | Low |
| [#14](https://github.com/NorbertAguilera/porfoleo_google/issues/14) | Dark mode toggle | Header switch + localStorage + no hydration flash | Low |
| [#15](https://github.com/NorbertAguilera/porfoleo_google/issues/15) | EN project images | All EN projects point to `cicloBnB.png` | Low |
| [#16](https://github.com/NorbertAguilera/porfoleo_google/issues/16) | Analytics | Privacy-friendly (Plausible / Umami) | Low |

### 🔵 Phase 4 — advanced (nice to have)

| Issue | Feature | Description | Effort |
|-------|---------|-------------|--------|
| [#17](https://github.com/NorbertAguilera/porfoleo_google/issues/17) | Project detail pages | Case studies with `[slug]` routes | Medium |
| [#18](https://github.com/NorbertAguilera/porfoleo_google/issues/18) | MDX blog posts | Frontmatter + syntax highlighting | Medium-High |
| [#19](https://github.com/NorbertAguilera/porfoleo_google/issues/19) | Skill levels | Expert / intermediate / basic indicators | Medium |
| [#20](https://github.com/NorbertAguilera/porfoleo_google/issues/20) | Testimonials | Quotes carousel | Low |
| [#21](https://github.com/NorbertAguilera/porfoleo_google/issues/21) | Scroll animations | Respect `prefers-reduced-motion` | Medium |
| [#22](https://github.com/NorbertAguilera/porfoleo_google/issues/22) | Loading skeletons | `loading.tsx` per route | Low |
| [#23](https://github.com/NorbertAguilera/porfoleo_google/issues/23) | Error boundaries | `error.tsx` with reset button | Low |
| [#24](https://github.com/NorbertAguilera/porfoleo_google/issues/24) | Newsletter signup | Buttondown / ConvertKit | Low |

---

## 🐛 Known bugs

| Issue | Description | Location |
|-------|-------------|----------|
| [#25](https://github.com/NorbertAguilera/porfoleo_google/issues/25) | "expierence" → "experience" | `dictonaries/*.json` |
| [#26](https://github.com/NorbertAguilera/porfoleo_google/issues/26) | "habilities" → "abilities" / "habilidades" / "habilitats" | `dictonaries/*.json` |
| [#27](https://github.com/NorbertAguilera/porfoleo_google/issues/27) | Nav label "Inicio" hardcoded | `components/Header.tsx` |
| [#28](https://github.com/NorbertAguilera/porfoleo_google/issues/28) | Duplicate images in `app/images/` and `public/images/` | `app/images/` |

---

## 🛠 Tech stack

| Category | Technology |
|----------|------------|
| Framework | Next.js 15, App Router |
| Language | TypeScript 5 |
| Styling | Tailwind CSS 4 |
| Fonts | Geist Sans & Geist Mono (`next/font`) |
| Icons | Heroicons, shields.io badges |
| i18n | Custom dictionary loader (3 locales) |
| Deployment | Vercel |

## 🌐 Internationalization

| Locale | Route | Dictionary |
|--------|-------|------------|
| Spanish | `/es/*` | `dictonaries/es.json` |
| English | `/en/*` | `dictonaries/en.json` |
| Catalan | `/ca/*` | `dictonaries/ca.json` |

To add a language: create `dictonaries/{lang}.json`, register it in `lib/dictonary.ts`, add it to `components/langSwitcher.tsx`, and update `next.config.ts` if needed.

---

## 📦 Deployment

Vercel: connect the GitHub repo for automatic deploys on push to `main`.

Manual: `npm run build && npm start`.

No env vars needed for the base site. For contact form and analytics:

```env
NEXT_PUBLIC_EMAILJS_SERVICE_ID=
NEXT_PUBLIC_EMAILJS_TEMPLATE_ID=
NEXT_PUBLIC_EMAILJS_PUBLIC_KEY=
NEXT_PUBLIC_PLAUSIBLE_DOMAIN=
```

## 🤝 Contributing

Fork, create a branch (`feature/issue-XX-description`), commit, push and open a PR. Pick an issue from Phase 1 to start.

## 📄 License

MIT.

## 📞 Contact

**Norbert Aguilera Capdevila**
- [LinkedIn](https://www.linkedin.com/in/norbert-aguilera-capdevila-553908278/)
- [GitHub](https://github.com/NorbertAguilera)
- [Portfolio](https://porfoleo-norbertaguilera.vercel.app/es)
