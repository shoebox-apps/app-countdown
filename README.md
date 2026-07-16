# Countdown

A big, live countdown to **September 30, 2026 — 00:00 Eastern Time**: the day Google's developer-verification requirement starts being *enforced* — first in Brazil, Indonesia, Singapore, and Thailand, expanding globally through 2027.

**Days until the door closes.** Ticking days / hours / minutes / seconds, every second — over a staged timeline (Verifier rollout → advanced-flow friction → Sept 30 enforcement → global). The door never fully shuts: apps still install over ADB, which is the whole point — one install through a door that stays open, and everything after is just a link.

Learn more and take action: [keepandroidopen.org](https://keepandroidopen.org)

## Run it

It's one file. Open `index.html` in any browser, or serve the repo root:

```
python3 -m http.server 8092
```

On a Shoebox host phone, add this repo's Pages URL and it appears in your launcher.

## Change the date

The target instant is a single constant at the top of the script in `index.html`:

```js
const TARGET_DATE_ISO = "2026-09-30T00:00:00-04:00"; // midnight ET (EDT, UTC-4)
```

Edit it, bump `version` in `manifest.json`, push — every phone running it gets prompted to deploy the new version.

## Files

- `index.html` — the whole app (inline CSS + JS, no dependencies)
- `manifest.json` — five fields; the contract the host reads
- `icon.png` — 512×512 launcher icon
- `.github/workflows/pages.yml` — deploys the repo root to GitHub Pages on push to `main`

MIT licensed.

## Add to Shoebox
Have the [Shoebox host](https://github.com/shoebox-apps/shoebox) installed? Scan this with your **phone's camera or Google Lens** — Shoebox opens with this app pre-filled, ready to add. No typing, no app store. (Your phone's camera does the scanning; Shoebox never asks for a camera permission.)

![Add to Shoebox](add-qr.png)

Or paste the base URL into Shoebox's **+ → Add**: `https://shoebox-apps.github.io/app-countdown/`

Fork it. Change one thing. Push. Watch your phone.
