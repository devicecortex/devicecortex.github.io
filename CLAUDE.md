# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML marketing website for Device Cortex, hosted on GitHub Pages. This repository is the source for www.devicecortex.com — any references to devicecortex.com are referring to this repo. Based on the Start Bootstrap "Modern Business" template. No build system, package manager, or CI/CD pipeline — just static HTML/CSS/JS served directly.

## Development

No build or install steps required. Open HTML files directly in a browser or use any local HTTP server:

```bash
python3 -m http.server 8000
```

The site deploys automatically via GitHub Pages when pushed to `main`.

## Tech Stack

- **Bootstrap 3** (CSS framework) with **jQuery** (JS)
- **Font Awesome 4** (icons)
- **Custom CSS**: `css/modern-business.css` (minimal overrides on top of Bootstrap)
- **Contact form**: `js/contact_me.js` sends AJAX POST to `bin/contact_me.php` — PHP won't execute on GitHub Pages, so the contact form is non-functional in production

## Site Structure

Three pages sharing a common Bootstrap navbar and footer pattern:

- `index.html` — Landing page with carousel, product showcase, app store links
- `zcastle.html` — Product page for zCastle smart home app (features, device compatibility)
- `contact.html` — Contact/support page with form and company info

## Key Conventions

- Pages use inline `<style>` blocks and shared external stylesheets (`css/bootstrap.min.css`, `css/modern-business.css`, `font-awesome/css/font-awesome.min.css`)
- Navigation and footer are duplicated in each HTML file (no templating system) — changes must be replicated across all pages
- Images live in `images/` with product screenshots, logos, and app store badges
- IE8 polyfills (HTML5Shiv, Respond.js) are included via CDN in each page's `<head>`
