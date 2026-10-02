# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

The marketing website for Arinoz Technologies (Pune). It is built on the "Sotech" HTML template from kodesolution.com, which was copied with **HTTrack** (see `arinoz/hts-log.txt`). There is no build system, package manager, framework, test suite or git repo. It is static HTML/CSS/jQuery plus a few PHP pages that use `include`, served by XAMPP's Apache.

- **Web root for the actual site:** `arinoz/html.kodesolution.com/2024/sotech-html/`. All real work happens here.
- `arinoz/index.html`, `backblue.gif`, `fade.gif`, `hts-cache/` and `hts-log.txt` are HTTrack artifacts, not part of the site.
- `arinoz.zip` (~56 MB) at the top level is a backup or archive of the mirror. Don't edit it.

## Running / checking

- Start Apache from the XAMPP control panel, then browse to
  `http://localhost/arinoz/arinoz/html.kodesolution.com/2024/sotech-html/<page>`. `.php` pages must be loaded through Apache, not opened as files, or the includes won't run.
- Syntax-check a PHP page: `/c/xampp/php/php.exe -l <file>.php`

## Page architecture

- **Custom Arinoz pages are `.php`** and share layout through includes:
  - `header.php` contains the full `<!DOCTYPE html><head>…` (stylesheets, meta, favicon), opens `<body><div class="page-wrapper">`, and renders the main, mobile and sticky headers.
  - `footer.php` contains the footer, closes `page-wrapper`/`body`, and loads **all JS** (jQuery, Bootstrap, plugins, then `js/script.js` last).
  - So a new page is: `<?php include 'header.php'; ?>` … page sections … `<?php include 'footer.php'; ?>`. `service.php` is the reference example. Don't add a second `<html>/<head>` around the include. `police-duty.php` currently does this and ends up with duplicated head/body markup.
- **The `.html` files are mostly untouched template demo pages** (`index-*`, `shop-*`, `page-*`, colour/RTL/dark variants). They are useful as a source of section markup to copy into PHP pages. They still have HTTrack "Mirrored from…" comments and links pointing back to the template site.
- **Navigation is defined once in `header.php` (`.main-menu .navigation`).** `js/script.js` clones that menu into `.mobile-menu` and `.sticky-header` at runtime, so those `<ul>`s are intentionally empty. Edit only the main menu.
- **Styling:** `css/style.css` is the template's stylesheet (~23k lines). Put Arinoz-specific overrides in `css/custom.css`, which loads after `style.css` in `header.php`, and scope rules tightly (e.g. `.header-style-two .header-lower …`) so template sections elsewhere aren't affected. Font Awesome 6 is loaded from cdnjs in addition to the template's bundled FA5.
- Animations use `wow` classes (`wow fadeInLeft` + `data-wow-delay`), which are initialised by `script.js`.

## Known in-progress gaps

These are referenced but don't exist yet. Create them or fix the links rather than assuming they exist:
- Includes in `service.php`: `Sidebar.php`, `components/Timeline2.php`, `components/help-box-button.php`, `components/clients-section.php` (there is no `components/` dir).
- Nav/footer targets: `index.php`, `our-servicess.php` / `our-services.php` (both spellings are used), `software-development.php`, `page-service-details-*.html`, `page-service-details-cloud` (no extension).
- `service.php` ends with `?` instead of `?>` after the footer include, which is a PHP parse error.
- The header search form still posts to the original kodesolution.com URL, and `footer.php` still has the template's Cloudflare email-decode and analytics beacon scripts.
