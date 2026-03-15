# Copilot Instructions for TechTyphoon

## Project Overview
TechTyphoon is a static website project structured with HTML, CSS, and JavaScript. The architecture is modular, with separate files for each page and feature. No backend or build system is present; all logic is client-side.

## Directory Structure
- `index.html`, `about.html`, `contact.html`, `project.html`, `work.html`: Main HTML entry points for each section.
- `css/`: Contains page-specific and shared CSS files. Use these for styling changes.
- `script/`: Contains JS files for each page and shared features (e.g., `anime.js`, `lenis-scroll.js`, `menu.js`).
- `public/`: Static assets (images, symbols) organized by feature/page.

## Key Patterns & Conventions
- **Page-specific logic**: Each page has a dedicated JS and CSS file (e.g., `about.js` and `about.css` for `about.html`).
- **Global styles**: Use `globals.css` for site-wide CSS rules.
- **Transitions & Animations**: Managed in `transition.js` and `anime.js`. Reuse these for new animated features.
- **Navigation/Menu**: Controlled via `menu.js` and styled in `menu.css`.
- **Image assets**: Organized by feature in `public/`. Reference images using relative paths in HTML/JS.

## Developer Workflows
- **No build step**: Directly edit HTML, CSS, and JS files. Changes are reflected immediately.
- **Preview**: Use a local static server (e.g., `npx serve .` or `python3 -m http.server`) from the project root to preview changes.
- **No tests**: There are no automated tests or test runners.
- **Debugging**: Use browser dev tools. Console logs are the primary debugging method.

## Integration Points
- **External dependencies**: Managed via CDN links in HTML or imported in JS (check HTML files for `<script src=...>` tags).
- **Vercel**: Deployment is configured via `vercel.json`.
- **Vite**: Project includes `vite.config.js` for local development, but no advanced build features are used.

## Examples
- To add a new page, create `newpage.html`, `css/newpage.css`, and `script/newpage.js`. Link the JS and CSS in the HTML file.
- For a new animation, add logic to `anime.js` or create a new JS file in `script/` and import as needed.

## References
- Main entry: `index.html`
- Shared logic: `script/anime.js`, `script/transition.js`, `script/menu.js`
- Global styles: `globals.css`
- Deployment: `vercel.json`

---
_If any conventions or workflows are unclear, please provide feedback so this guide can be improved._
