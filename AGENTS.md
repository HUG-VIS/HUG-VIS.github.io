# Repository Guidelines

## Project Structure & Module Organization

This repository is a dependency-free, single-page GitHub Pages site. `index.html` contains the page structure and benchmark copy, `styles.css` owns all responsive layout and visual styling, and `script.js` provides navigation, reveal animations, gallery switching, the lightbox, and BibTeX copying. Store web-ready figures in `images/site/`; `images/main_2.png` is used by the README. Root-level files such as `README.md`, `robots.txt`, `sitemap.xml`, `.nojekyll`, and the academic-use license support documentation and deployment. There is currently no separate build, source, or test directory.

## Build, Test, and Development Commands

No package installation or compile step is required.

- `python3 -m http.server 8000` — serve the repository locally.
- Open `http://localhost:8000/` — review the site through HTTP rather than `file://`.
- `git diff --check` — detect trailing whitespace and malformed patch lines before committing.

GitHub Pages publishes the checked-in static files directly from the repository root.

## Coding Style & Naming Conventions

Use two-space indentation in HTML, CSS, and JavaScript. Keep HTML semantic and preserve accessibility details such as meaningful `alt` text, labels, focus behavior, and `aria-*` state. Use kebab-case for CSS classes and `data-*` hooks (for example, `.hero-stats` and `data-lightbox`). JavaScript uses `const` by default, single-quoted strings, semicolons, optional chaining where appropriate, and small event-driven blocks. Reuse CSS custom properties from `:root` and existing responsive breakpoints before adding one-off values. Optimize large figures and prefer `.webp` for page imagery.

## Testing Guidelines

There is no automated test framework or coverage requirement. For every UI change, test desktop and narrow mobile widths. Verify header scrolling, mobile navigation, active-section highlighting, gallery tabs, lightbox open/close behavior, and the citation copy button. Check the browser console for errors and confirm that edited image, download, canonical, and social-preview paths resolve.

## Commit & Pull Request Guidelines

The current history uses a short, imperative, sentence-case subject (`Add HUG-VIS project page`). Follow that pattern and keep each commit focused. Pull requests should summarize the user-visible change, list manual checks, link any relevant issue, and include desktop and mobile screenshots for layout changes. Call out newly added large binary assets and avoid mixing unrelated content or formatting changes.
