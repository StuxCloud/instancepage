<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.cloud/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.cloud/logo-dark.png"><img src="https://global.media.stux.cloud/logo-dark.png" height="100" alt="Stux.Cloud Logo"></picture>
</p>

# Instance Page

### *Powering everything, quietly & securely!*

A clean and simple instance landing page template for Stux.Cloud projects.

## Overview

This repository contains a lightweight HTML landing page designed to announce Stux.Cloud instances or services. It's perfect for maintaining audience engagement while your project is in development.

## Features

- 📄 Simple, clean HTML structure
- ⚡ Lightweight and fast-loading
- 🎨 Ready to customize
- 📱 Responsive design
- 🚀 Deployed at [instancepage.stux.cloud](https://instancepage.stux.cloud)

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/StuxCloud/instancepage.git
   ```

2. Run it locally:
   ```bash
   ./dev-server.sh        # or dev-server.bat on Windows
   ```
   Then open the printed `http://127.0.0.1:8000` URL. You can also just open `index.html` directly in your browser, or deploy it to your hosting provider.

## Customization

Edit the HTML files to:
- Update the instance message
- Add your branding and logo
- Customize colors and styling
- Include email signup or social links

## Deployment

This project uses GitHub Pages and can be automatically deployed to your desired domain.

The live version is deployed at [instancepage.stux.cloud](https://instancepage.stux.cloud).

## Previous designs

This repository always holds the current Stux.Cloud design (v3, single teal `#07878e`). Earlier designs are preserved as their own archived repositories:

- [instancepage-v1](https://github.com/StuxCloud/instancepage-v1): the original blue design, live at [instancepage-v1.stux.cloud](https://instancepage-v1.stux.cloud/)
- [instancepage-v2](https://github.com/StuxCloud/instancepage-v2): the two-tone green design, live at [instancepage-v2.stux.cloud](https://instancepage-v2.stux.cloud/)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to get involved, and [CHANGELOG.md](CHANGELOG.md) for release history.

## License

Copyright (c) 2026 Stux.Group. This project is open source and available for use and modification.

---

*Built & Maintained by <img src="https://github.com/StuxCloud.png" height="14" alt="Stux.Cloud" valign="middle"> [Stux.Cloud](https://github.com/StuxCloud), Hosted by <img src="https://github.com/Stuxedo.png" height="14" alt="Stuxedo" valign="middle"> [Stuxedo](https://stuxedo.com).    
Stux.Cloud is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" alt="Stux.Group" valign="middle"></picture> Stux.Group brand of businesses.*

## Local preview

Run `./dev-server.sh` (or `dev-server.bat`, add a port as the last argument) to serve the site at `http://127.0.0.1:8000` the way GitHub Pages does, with the dev-mode banner on. Add `--no-dev-mode` to see it exactly as production does, or `?banner=soon,maintenance,site` to preview the other banner types. It uses PHP 7.4's built-in server (set `PHP_BIN` to pick another PHP).
