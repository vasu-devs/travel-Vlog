# travel-Vlog

A lightweight, static travel vlog website showcasing trips across India. This repository contains simple HTML pages for destinations, CSS for styling, and image/video assets — ready to be viewed locally or deployed to GitHub Pages.

## Table of contents

- [Demo](#demo)
- [Features](#features)
- [Getting started](#getting-started)
- [Serve locally](#serve-locally)
- [Deploy to GitHub Pages](#deploy-to-github-pages)
- [Project structure](#project-structure)
- [Notes & recommended fixes](#notes--recommended-fixes)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Demo

Open `index.html` in your browser to view the site locally. For a better experience serve the folder with a simple HTTP server (instructions below).

If you'd like, I can add a deployed GitHub Pages demo and include a live link here.

## Features

- Pure static site: plain HTML, CSS and images (no build step)
- Individual pages for many destinations (for example `Goa.html`, `Hampi.html`, `Munnar.html`)
- Image assets in the `image/` directory and a placeholder `video/` directory for videos
- Minimal JavaScript used for login behavior (`login.js`) if present

## Getting started

Requirements: a modern browser. For local serving you can use Python (comes preinstalled on many systems) or Node.js.

## Serve locally

Recommended: run a simple HTTP server and open the site at http://localhost:8000.

In PowerShell (Windows) with Python 3 installed:

```powershell
# serve current directory at http://localhost:8000
python -m http.server 8000

# then open http://localhost:8000/index.html
```

Or using Node.js (no global install required):

```powershell
npx http-server -c-1 -p 8000

# then open http://localhost:8000/index.html
```

Opening `index.html` directly works too, but a local server avoids cross-origin issues for some browsers and provides a closer match to hosting.

## Deploy to GitHub Pages

An easy option is to publish the repository's `master` (or `main`) branch to GitHub Pages.

1. Push your repo to GitHub under `username/travel-Vlog`.
2. On GitHub: Repository > Settings > Pages. Under "Source", choose the branch (e.g., `master`) and save.
3. After a minute, your site will be available at `https://<username>.github.io/travel-Vlog/`.

Alternative (recommended for single-branch workflow): use the `gh-pages` npm package to publish the built site to the `gh-pages` branch — useful if you later add a build step.

If you want, I can add a small GitHub Actions workflow to build/deploy automatically (currently unnecessary because the site is static).

## Project structure

Top-level files and directories (abridged):

- `index.html` — home page
- `*.html` — destination pages (e.g. `Goa.html`, `Amritsar.html`, `Munnar.html`)
- `style.css`, `place.css`, `menu .css`, `login.css`, `south india.css`, `north india.css`, `north east.css` — stylesheets
- `login.html`, `login.js` — login UI and script
- `image/` — images used on the site
- `video/` — video assets (currently placeholder)

Note: some filenames contain spaces (for example `menu .css` and `Ziro Valley.html`). These work locally but are better renamed for portability and to avoid potential tooling/URL issues.

## Notes & recommended fixes

Here are low-risk improvements you might consider:

- Normalize filenames: remove spaces and use hyphens (e.g., `ziro-valley.html`, `menu.css`).
- Consolidate and minify CSS to simplify maintenance and reduce page load.
- Move JS to a `js/` folder and CSS to `css/` for clearer structure.
- Add `alt` attributes to images where missing for accessibility and SEO.
- Add responsive images (`srcset`) to improve performance on mobile.

If you want, I can apply these changes in a separate PR (I can make them one at a time so it's easy to review).

## Contributing

Contributions are welcome. Suggested workflow:

1. Fork the repository
2. Create a feature branch: `feature/your-change`
3. Commit changes with a clear message
4. Open a pull request describing the change and why

For large refactors (layout, build tooling), please open an issue first so we can discuss scope.

## License

This repository does not currently include a `LICENSE` file. If you'd like me to add an open-source license I recommend the MIT license for permissive use. Tell me if you want MIT, Apache-2.0, or another license and I will add it.

## Contact

Repository owner: `vasu-devs`.

If you'd like, I can:

- add a `LICENSE` file (e.g., MIT)
- normalize filenames and update links across HTML files
- add a basic GitHub Actions workflow to deploy to GitHub Pages automatically

Tell me which of the above you want next and I'll implement it.

---

_Small note:_ I kept the README focused and GitHub-friendly. If you want a README that includes screenshots, add a `screenshots/` folder or point me to images to include and I will add them with relative links.
