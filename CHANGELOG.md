# Changelog

All notable changes to instancepage are documented here.

## v3.0.2

### Changed

- The footer no longer says "Stux.Cloud is operated by Stux Group Ltd."; that belongs on the Imprint, which still says it. The copyright line names Stux.Cloud ("© 2026 Stux.Cloud. All rights reserved.") instead of Stux.Group

## v3.0.1

### Fixed

- The light/dark choice was saved in the browser under `stuxedo-theme`, a name left over from the Stuxedo page this one was built from; it's now `stuxcloud-theme` on every page, and the Cookies Policy names it correctly. A theme picked before this update resets to the system setting once

## v3.0.0

### Changed

- Rebranded from Stux.Cloud's two-tone green to the single teal `#07878e`, which reads at about 4.1:1 on both the dark and light themes. Every green accent, gradient stop, floating-particle shade and site-banner accent is now `#07878e`; the dark and light backgrounds and text shift from green-tinted to teal-tinted (`#031d1e`, `#e6feff`, `#eef2f2`); button hover is a slightly brighter `#0a9ea6`
- The logo, icon and favicon pick up the new teal Stux.Cloud assets automatically from `global.media.stux.cloud`
- README links the archived earlier designs: [instancepage-v1](https://github.com/StuxCloud/instancepage-v1) (the original blue design); [instancepage-v2](https://github.com/StuxCloud/instancepage-v2) (the two-tone green design)

## v1.3.2

### Changed

- The footer's copyright year is worked out automatically: the start year alone in the first year, then START–CURRENT

## v1.3.1

### Changed

- The copyright line reads Stux.Group instead of Stux Group Ltd

### Fixed

- The footer's Created-with icons are optically sized, so the heart no longer looks bigger than the code and coffee icons

## v1.3.0

### Added

- A dev-mode banner, the shared Stux site banner, shown on every page while `dev-server.sh`/`.bat` runs; `?banner=soon,maintenance,site` previews the other banner types locally, and production never shows one (`assets/site-banner.css`, `assets/site-banner.js`, `assets/site-banners.js`, `assets/dev-mode.js`)
- A "Created with love / code / coffee by Stux.Cloud" line in the footer of every page
- `/sitemap` (an HTML page in the site's layout listing every page) and `sitemap.xml`, committed as static files and regenerated with `python scripts/build-sitemap.py` (`lastmod` comes from each page's last git commit); `robots.txt` points at it and the footer links to it

### Changed

- `dev-server.sh`/`.bat` serve the site the way GitHub Pages does (`/changelog` for `changelog.html`, the 404 page for missing paths) through `.github/dev-router.php`, turn DEV_MODE on by default (`--no-dev-mode` to preview production), and run on PHP 7.4 like the other Stux projects (`PHP_BIN`, `php74`, or `%LOCALAPPDATA%\Programs\PHP\7.4`, with a warning otherwise)
- The copyright symbol in the footers is an icon, with a visually hidden "©" so screen readers still read it

### Removed

- The "Powered by Stuxedo" badge in the footer: this page is served by GitHub Pages (see `CNAME`), not by Stuxedo hosting

## v1.2.0

### Added
- A "Boring Legal Stuff" legal hub (`legal.html` + `legal/`: privacy, terms, cookies, imprint, disclaimer, opt-out), matching the Stuxedo instance page

### Changed
- `changelog.html` now sorts each release's `###` sections into a fixed order — Added, Changed, Fixed, Removed, Security, Deprecated — at render time, rather than trusting the order `CHANGELOG.md` lists them in; unknown section types go last
- Changelog type badges now use the fixed family palette — Added `#2ecc71`, Changed `#3ba7ff`, Fixed `#ffa64d`, Removed `#ff4d4d`, Security `#b06bff`, Deprecated `#8a8a94` — as tinted badges (coloured text on a light tint of the same hue), with darker variants of each for the light theme

### Fixed
- The footer's "Boring Legal Stuff" link pointed at `https://stux.cloud/legal`, which returns a 404 — it now opens this page's own legal hub

## v1.1.3

### Fixed
- The footer's changelog/version link (and other footer links) turned accent-purple once visited — `a:visited` carries a pseudo-class, giving it higher CSS specificity than the plain `footer a` selector meant to keep footer links muted, so it kept winning regardless of source order. Every affected footer link now also styles `footer a:visited` explicitly.

## v1.1.2

### Fixed
- The header tagline still read the old "Powered by Stuxedo" line instead of the current org-wide tagline, "Powering everything, quietly & securely", used on the other Stux.Cloud pages (soonpage, maintenancepage). The "Powered by Stuxedo" hosting badge lower on the page is unrelated and unchanged.

## v1.1.1

### Fixed
- GitHub Pages was using the legacy branch-deploy build system, which can silently stop auto-deploying with no error recorded anywhere (discovered on SeasonalOverlaysLibrary — its live site served stale content for over an hour with no visible failure). Switched to GitHub Actions-based Pages deployment (`.github/workflows/pages.yml`), making every deploy an ordinary, observable CI run instead.

## v1.1.0

### Added

- Self-hosted Exo 2, Barlow and Inter font files under `assets/fonts/`, replacing the Google Fonts CDN link
- `changelog.html`, which fetches and renders `CHANGELOG.md` at runtime
- A version indicator in the footer, next to the existing "Boring Legal Stuff" link, fetched live from `VERSION.md`
- Cross-origin `postMessage` title sync, so a page embedding this one in an iframe can mirror this page's `<title>`
- A custom `404.html` error page

## v1.0.7

### Added
- Stux.Cloud's slogan, "Powering everything, quietly & securely!", added to `README.md`.

## v1.0.6

### Fixed
- `README.md`'s License section named `Stux.Group` (a brand, not a legal entity) as the copyright holder — corrected to `Stux Group Ltd`.

## v1.0.5

### Fixed
- `README.md`'s and `index.html`'s own Stux.Cloud logo/favicon (separate from the Stux.Group brand icon already fixed in v1.0.4) still pointed at the old `media.stux.cloud/global/logo.png` (and `/icon.png`) host — corrected to `https://global.media.stux.cloud/logo.png` and `/icon.png`

## v1.0.4

### Fixed
- `README.md`'s Stux.Group brand icon URL had a leftover duplicated `/global/` path segment (`global.media.stux.group/global/icon.png`) — corrected to `https://global.media.stux.group/icon.png`

## v1.0.3

### Changed
- `CONTRIBUTING.md`'s general contact address changed from `contact@stux.cloud` to `hello@stux.cloud`, matching the convention used across other Stux.Group brand repos

## v1.0.2

### Changed
- `README.md`'s footer/brand-attribution block updated to the new two-line format (Built & Maintained by Stux.Cloud, Hosted by Stuxedo / Stux.Cloud is a part of the Stux.Group brand of businesses), replacing the older single-line disclaimer and the redundant separate "Made by Stux.Cloud" line

## v1.0.1

### Added
- The Stux.Group icon now appears inline next to the "part of the Stux.Group Brand of Companies" line in `README.md`, alongside the existing Stux.Cloud logo

## v1.0.0

### Added
- `VERSION.md`, `CHANGELOG.md`, and `CONTRIBUTING.md`
- A `commit.sh`/`commit.bat` pair that reads the version from `VERSION.md` and tags the release accordingly
- A `dev-server.sh`/`dev-server.bat` pair to serve the page locally without hand-configuring a static server
- A "Boring Legal Stuff" footer link on the instance page, pointing to `https://stux.cloud/legal`
