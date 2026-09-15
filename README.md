# Playwright Chromium Bundle

This repository distributes the Playwright Chromium browser bundle downloaded from the official Playwright CDN.

## Included versions

- Chrome for Testing / Chromium: `151.0.7922.34` (Playwright Chromium revision `1234`)
- FFmpeg: Playwright revision `1011`
- Chrome Headless Shell: `151.0.7922.34` (Playwright revision `1234`)

The complete binary bundle is published as a GitHub Release asset rather than committed to Git, because the archive is larger than GitHub's standard repository file-size limit.

## Download

Download `playwright-chromium-bundle-linux-x64.tar.gz` from the Releases page, then extract it into a Playwright cache directory:

```bash
mkdir -p "$HOME/.cache/ms-playwright"
tar -xzf playwright-chromium-bundle-linux-x64.tar.gz -C "$HOME/.cache/ms-playwright"
```

The extracted directories are:

- `chromium-1234`
- `chromium_headless_shell-1234`
- `ffmpeg-1011`

## Verification

After extraction, verify the main executable exists:

```bash
test -x "$HOME/.cache/ms-playwright/chromium-1234/chrome-linux64/chrome"
"$HOME/.cache/ms-playwright/chromium-1234/chrome-linux64/chrome" --version
```

## Source

The files were downloaded using Playwright's `playwright install chromium` command, which retrieves the browser components from Playwright's official CDN.
