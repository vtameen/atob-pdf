# AtoB PDF

**A fully offline PDF toolkit for Windows and macOS.** Every tool runs on your own computer - no uploads, no internet needed, no accounts. Your documents never leave your machine.

## Download

Go to the **[latest release](../../releases/latest)** and download the installer for your system:

| System | File |
|---|---|
| Windows 10 / 11 | `AtoB PDF Setup 3.2.0.exe` |
| macOS (Intel + Apple Silicon) | `AtoB PDF-3.2.0-universal.dmg` |

## Install

### Windows
1. Download the `.exe` and double-click it.
2. If Windows SmartScreen appears, click **More info**, then **Run anyway** (the app is unsigned - this warning is normal).
3. Follow the installer. AtoB PDF appears in the Start menu and can open PDFs directly.
4. Bonus: select several PDFs in Explorer, right-click, and choose **Merge in AtoB PDF**.

### macOS
1. Download the `.dmg`, open it, and drag **AtoB PDF** into Applications.
2. First launch only: **right-click the app > Open**, then click **Open** again (unsigned app - macOS asks once).

## About

AtoB PDF is an Acrobat-style, offline-first PDF app:

- **View & edit** - full reader with search and print, in-place text editing, add text, whiteout, highlight, shapes, images, sticky notes, true redaction
- **Pages** - merge, split, extract, delete, rotate, crop, and drag-and-drop organize
- **Convert** - PDF to Word/text/images, Word/text/images to PDF, OCR (make scanned PDFs searchable)
- **Sign & forms** - draw/type/upload a signature, fill PDF forms
- **Secure & optimize** - password protect, unlock, compress, flatten, repair damaged files

Everything works with no internet connection. There is no telemetry and no server: the app is a self-contained bundle of open-source engines (PDF.js, pdf-lib, MuPDF, Tesseract OCR) with its own editor UI.

## Build from source

The full source is in this repository (`atob-pdf-payload.zip`). Every push to `main` builds both installers automatically via GitHub Actions - see `.github/workflows/build.yml`. To build locally: unzip the payload, run `node build.mjs`, then `npm install && npm run dist` inside `electron/`.

## Licensing

AtoB PDF bundles MuPDF (AGPL-3.0), PDF.js (Apache-2.0), pdf-lib (MIT), and Tesseract.js (Apache-2.0). The complete corresponding source is published in this repository. If you plan to sell a derivative, you must keep the source available under AGPL-3.0 or obtain a commercial MuPDF license from Artifex.
