# CLAUDE.md

## Project Overview

Official Google Chrome Extensions sample repository. Contains two categories of samples:

- **`api-samples/`** — minimal extensions focused on demonstrating a single Chrome Extension API
- **`functional-samples/`** — full-featured extensions spanning multiple APIs
- **`_archive/mv2/`** — legacy Manifest V2 samples (read-only reference)
- **`_archive/apps/`** — deprecated Chrome Apps platform (read-only)

All new samples target **Manifest V3**.

## Development Commands

```bash
npm install          # Install dev tooling (ESLint, Prettier, husky)
npm run lint         # ESLint all .js files
npm run lint:fix     # Auto-fix lint errors
npm run prettier     # Format .md, .html, .json files
```

Pre-commit hooks (husky + lint-staged) run lint and prettier automatically on staged files.

## Loading a Sample in Chrome

1. Open `chrome://extensions`
2. Enable **Developer mode** (top-right toggle)
3. Click **Load unpacked** and select the sample's directory

## Extension Structure Convention

Each sample is a self-contained directory with a `manifest.json`. Typical layout:

```
api-samples/<api-name>/<sample-name>/
  manifest.json    # Required: declares permissions, background, etc.
  popup.html       # Optional: extension popup
  background.js    # Optional: service worker (MV3)
  content.js       # Optional: content script
  icons/           # Extension icons
  README.md        # What this sample demonstrates
```

## Key Conventions

- All new samples must use **Manifest V3** (`"manifest_version": 3`)
- Service workers replace background pages — no persistent background scripts
- Use `chrome.action` API (not `chrome.browserAction`)
- Each sample directory must be independently loadable as an unpacked extension
- ESLint config is in `eslint.config.js` at the repo root — don't add per-sample `.eslintrc` files
- Don't add `node_modules` or build artifacts to sample directories

## Adding a New Sample

1. Create a directory under `api-samples/` or `functional-samples/`
2. Include a valid `manifest.json` with `"manifest_version": 3`
3. Add a `README.md` explaining what API(s) the sample demonstrates
4. Run `npm run lint` and `npm run prettier` before committing
