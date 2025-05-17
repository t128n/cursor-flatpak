# Cursor Flatpak

| Build Type | Status |
|------------|---------|
| Latest | [![Cursor Flatpak](https://github.com/t128n/cursor-flatpak/actions/workflows/flatpak.yml/badge.svg)](https://github.com/t128n/cursor-flatpak/actions/workflows/flatpak.yml) |
| Automated | [![Cursor Flatpak](https://github.com/t128n/cursor-flatpak/actions/workflows/flatpak.yml/badge.svg?event=schedule)](https://github.com/t128n/cursor-flatpak/actions/workflows/flatpak.yml) |

Automatic Flatpak packaging for [Cursor](https://cursor.com/), the AI-first code editor.

## About

This repository automatically packages the latest version of Cursor as a Flatpak. The GitHub Actions workflow runs every 12 hours to check for new versions and builds a new Flatpak when updates are available.

## Installation

### Install from GitHub Releases

1. Go to the [Releases page](https://github.com/t128n/cursor-flatpak/releases)
2. Download the latest `.flatpak` file
3. Install it using:

```
flatpak install --user ./com.cursor.Cursor-VERSION.flatpak
```

## Running

After installation, you can run Cursor with:

```bash
flatpak run com.cursor.Cursor
```

## How It Works

The automated build process:
1. Checks for new Cursor versions every 12 hours
2. Downloads the official Linux AppImage when a new version is available
3. Extracts and packages it as a Flatpak
4. Creates a new GitHub release with the Flatpak package