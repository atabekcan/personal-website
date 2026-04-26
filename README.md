# atabekyucel.com

Personal website for Atabek C. Yucel — VP of Product / CPO-scope executive in AI & Digital Health.

Built as a static single-page site with a lightweight localStorage-backed CMS admin panel. No frameworks, no build step — just HTML, CSS, and vanilla JS.

## Structure

```
.
├── index.html      # Main site (public-facing)
├── admin.html      # CMS admin panel (password-protected)
├── .claude/
│   └── launch.json # Local dev server config
└── README.md
```

## Local Development

Requires [Node.js](https://nodejs.org) for the preview server.

```bash
npx serve -p 3456 .
```

Then open [http://localhost:3456](http://localhost:3456) in your browser.

## Content Management

Navigate to `/admin.html` and enter the password to access the CMS panel.

- **Portfolio tab** — add, edit, reorder, and delete portfolio cards across four categories: Professional Products, VibeCoded Products, Board Memberships, and Projects
- **Hero tab** — edit the badge, subtitle, description, and stats displayed in the hero section
- **Contact tab** — update email, LinkedIn URL, and the contact tagline

All content is stored in `localStorage` under the key `acy_site_content`. Use the **Export** button to download a JSON backup and **Import** to restore it.

> **Note:** localStorage is browser-scoped. To share content changes across devices or browsers, export the JSON and re-import it on the target browser.

## Deployment

The site is fully static — no server-side logic required. Drop the files into any static host:

- [Vercel](https://vercel.com) — `vercel deploy`
- [Netlify](https://netlify.com) — drag-and-drop or CLI
- [GitHub Pages](https://pages.github.com) — push to `main`, enable Pages in repo settings

## Tech

- Vanilla HTML / CSS / JavaScript
- [Inter](https://rsms.me/inter/) + [JetBrains Mono](https://www.jetbrains.com/legalforms/mono/) via Google Fonts
- CSS custom properties, glassmorphism, Intersection Observer animations
- `localStorage` for CMS persistence
- `sessionStorage` for admin auth gate

## License

MIT — see [LICENSE](LICENSE).
