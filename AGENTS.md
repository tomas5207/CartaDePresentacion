# AGENTS.md

## What this is

Single-page static HTML portfolio site. No build system, no bundler, no framework.

## Structure

- `index.html` — the entire site (all markup, inline `<style>`, inline JS)
- `Estilos/estilos.css` — external stylesheet (older/alternate styles, partially superseded by inline styles in `index.html`)
- `bootstrap-5.3.2-dist/` — Bootstrap 5 dist (CSS + JS), vendored locally
- `Fuentes/` — local fonts: Bebas_Neue, Orbitron, Cormorant-Garamond
- `Iconos/` — PNG icons used in the site
- `Imagenes/` — photos, project screenshots, backgrounds
- `Tomás Jorcin CV*.pdf` — downloadable CV files (Spanish + English)

## How to preview

Open `index.html` directly in a browser, or use the VS Code launch config (`.vscode/launch.json`) which opens it in Chrome.

## Key conventions

- **Language**: Site is in Spanish (`lang="es"`). Keep content in Spanish unless explicitly changing language.
- **Styling**: Tailwind CSS loaded via CDN (`cdn.tailwindcss.com`). Most styling is inline Tailwind classes + a large `<style>` block in `index.html`. The external `Estilos/estilos.css` is an older stylesheet — some classes overlap. When editing styles, prefer the inline `<style>` in `index.html` as the source of truth.
- **Fonts**: Custom `@font-face` declarations reference `../Fuentes/` paths. Font references in `index.html` use relative paths from root; in `Estilos/estilos.css` they use `../Fuentes/`.
- **Content**: This is a personal portfolio for Tomás Jorcin Rodriguez. Sections: hero, timeline/career, about me, projects, services, contact, footer.
- **No npm**: `package.json` is empty. `node_modules/` can be ignored.
- **No tests, no lint, no build**: There are no dev commands to run.
