# Changelog

All notable changes to instancepage are documented here.

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
