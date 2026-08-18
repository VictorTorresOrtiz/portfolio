# Portfolio (Braxton template)

Static HTML portfolio/resume site. Braxton HTML template, customized as personal portfolio. No build step, no framework, no package.json — edit files directly, open `index.html` in browser to preview.

## Structure

- `index.html` — single page, all sections (loader, header, hero, about, resume, portfolio/gallery, contact form, footer). Big file, ~900+ lines.
- `css/main.css` — site-specific styles (edit this for custom changes).
- `css/plugins.css` — third-party plugin styles, don't hand-edit.
- `css/main-demo.css`, `css/plugins-demo.css` — template-demo-only styles (color switcher, etc), likely prunable for production.
- `js/app.js` — site behavior/init.
- `js/gallery-init.js` — portfolio gallery/swiper init.
- `js/libs.min.js` — bundled third-party JS libs.
- `js/demo/` — template demo-switcher scaffolding, not needed for real deployment.
- `mail.php` — contact form backend (PHP mail). Needs a PHP host to work.
- `source-files/` — original/unminified vendor sources (swiper, braxton css). Reference only, not served.
- `fonts/`, `img/` — static assets.

## Working here

- No bundler/transpiler. Changes to `index.html`/`css`/`js` are live on refresh.
- Keep custom edits in `main.css`/`app.js`, not the `plugins*`/`libs.min.js` vendor files.
- `mail.php` builds email HTML from `$_POST`/`$_GET` directly — don't add fields without escaping output (it currently interpolates raw form values into HTML, XSS risk if ever reflected).
- Demo-only files (`*-demo.css`, `js/demo/`, color switcher UI in header) are template scaffolding for showcasing color variants — fine to strip when this becomes the final deployed site.
