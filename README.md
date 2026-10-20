# ER-Releases

This repository is used to publish and host releases for the
[`ZUGFeRD-invoice-generator`](https://github.com/SebastianKungl/ZUGFeRD-invoice-generator)
project (ZUGFeRD Rechnungen). The source code is private; this repo exists so
the Windows installer can be downloaded without a login.

## Download

**[Latest release](https://github.com/SebastianKungl/ER-Releases/releases/latest)** –
download `ZUGFeRD-Rechnungen-Setup-x.y.z.exe` from its assets.

## Installation

1. Run the Setup `.exe`. Windows SmartScreen may warn "Windows protected your
   PC" – click **More info** → **Run anyway** (the app has no paid code-signing
   certificate).
2. The app installs per-user into `%LOCALAPPDATA%\Programs\ZUGFeRD-Rechnungen`
   (no admin rights needed), adds a Start Menu entry and an optional Desktop
   shortcut, and opens in the browser.

## Updates

On start the app checks this repo for a newer release and shows the release
notes in a banner. **Jetzt aktualisieren** installs the update and restarts the
app. Invoices, customers and settings in `%APPDATA%\ZUGFeRD Rechnungen` are kept.

## Publishing (maintainer notes)

Releases are written by the GitHub Actions workflow in the source repo
(`.github/workflows/release.yml`) on a `vx.y.z` tag, using a fine-grained PAT
scoped to this repo with `Contents: Read and write`, stored there as the
`RELEASES_TOKEN` secret.
