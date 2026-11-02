# Lawn Equipment Log

[![Latest release](https://img.shields.io/github/v/release/H4W9/lawn-equipment-log?style=flat&color=2d6a37&label=release&cacheSeconds=1800)](https://github.com/H4W9/lawn-equipment-log/releases/latest)
[![Total downloads](https://img.shields.io/github/downloads/H4W9/lawn-equipment-log/total?style=flat&color=2d6a37&label=downloads&cacheSeconds=1800)](https://github.com/H4W9/lawn-equipment-log/releases)
[![Live demo](https://img.shields.io/badge/live-demo-2d6a37?style=flat&logo=githubpages&logoColor=white)](https://h4w9.github.io/lawn-equipment-log/)

A single-file HTML tool for keeping maintenance records on lawn equipment:
riding mowers, zero-turns, push mowers, trimmers, blowers, chainsaws and more.
Track serial and model numbers, engine details, part numbers, fluids, purchase
info and the hour meter for each machine, set service intervals by hours and/or
days, and log every service. Anything overdue or due soon is flagged at a glance.

**Live demo:** https://h4w9.github.io/lawn-equipment-log/

**Download the latest release:**
https://github.com/H4W9/lawn-equipment-log/releases/latest/download/lawn-equipment-log.html

## Features

- Equipment list sorted by what needs attention first (Overdue, Due soon, OK)
- Per-machine page: hour meter, maintenance schedule, specs & parts, service history
- Suggested service schedules for each equipment type, fully editable
- Logging a service resets the selected intervals and updates the hour meter
- Search by name, make, model or serial number; filter by equipment type
- Backup & restore: export to a `.json` file or copied text, import on another
  device (merge or replace)
- Light and dark mode, works on phones

## Open it

Double-click **`lawn-equipment-log.html`**. It runs in any browser. No install,
no internet needed (fonts load from Google Fonts when online and fall back to
system fonts offline).

It opens with three example machines so you can see how it works. Tap
**Remove examples** to clear them.

## Privacy & where your data lives

Everything runs in your browser. There are no accounts and no data is sent
anywhere. Equipment and service records are saved in the browser's
`localStorage` on that device only.

That storage is tied to the browser **and** the page's location. The live demo
URL and a downloaded copy of the file each keep separate data, and a copy saved
under a different name or folder starts empty. Use **Backup & restore** to move
data between devices, browsers or copies, and to keep a safe backup.

## Releases & deployment

GitHub Pages is deployed by `.github/workflows/pages.yml` on every push to
`main`. One-time setup after the first push:

**Settings → Pages → Build and deployment → Source: "GitHub Actions"**

To cut a release:

```bash
# 1. Bump the version in lawn-equipment-log.html:
#      <meta name="app-version" content="1.0.1">
# 2. Commit it to main, then:
git tag v1.0.1
git push origin v1.0.1
```

Pushing a `vX.Y.Z` tag runs `.github/workflows/release.yml`, which stamps the tag
version into the page and publishes a GitHub Release with `lawn-equipment-log.html`
and `lawn-equipment-log.zip` attached. It can also be run by hand from the
**Actions** tab.

## Files

| File | What it is |
|------|-----------|
| `lawn-equipment-log.html` | The entire tool: HTML, CSS, and JS in one file |
| `apple-touch-icon.png` | Home-screen icon used when saved to a phone |
| `index.html` | Tiny redirect to the tool, so Pages serves it at the repo root |
| `.github/workflows/pages.yml` | CI: push to `main` → deploy to GitHub Pages |
| `.github/workflows/release.yml` | CI: tag → GitHub Release |
| `README.md` | This document |
