# Contributing to instancepage

Thank you for your interest in contributing! This repository is a small, static instance-landing-page template, so contributions are usually small too.

## Getting Started

1. **Fork the repository** and clone your fork locally.
2. **Run it locally** with `./dev-server.sh` (or `dev-server.bat` on Windows) and open the printed URL.
3. **Make your changes** to `index.html` — it's a single self-contained file, no build step required.
4. **Submit a pull request** with a clear description of what you've changed and why.

## Reporting Bugs

- Check existing issues to avoid duplicates before opening a new one.
- Provide a clear title and description, steps to reproduce, and the expected vs. actual behaviour.
- Include your browser and OS where relevant — this is a purely client-side page, so most bugs are rendering issues.

## Suggesting Features

- Open an issue with the label `enhancement` and describe your idea clearly.
- Keep in mind this project is meant to stay lightweight and dependency-free.

## Style Guidelines

- Keep `index.html` a single static HTML file where possible — no build tooling, no frameworks. `changelog.html`, `404.html` and `assets/fonts/` are the deliberate exceptions: fonts need real files to self-host, and `changelog.html` fetches and renders `CHANGELOG.md` at runtime rather than duplicating it inline.
- Match the existing CSS variable naming and light/dark theme structure.
- General contact uses `hello@stux.cloud`; the legal hub lives externally at `https://stux.cloud/legal`, not in this repo.
- Test both the light and dark themes, and the embedded (iframe) code path, before submitting.

## Questions

If you have any questions, feel free to reach out at [hello@stux.cloud](mailto:hello@stux.cloud) or open a discussion in this repository.

---

*Stux.Cloud is part of the [Stux.Group](https://github.com/StuxGroup) Brand of Companies.*
