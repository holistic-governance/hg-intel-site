# hg-intel-site

Public standalone repo for the **HG Intel** website — regulatory & best-practice intelligence for
Australian healthcare. This repo **is the source of truth** for the site and is served via
**GitHub Pages** at **https://hg-intel.com.au**.

Local clone: `~/work/holistic-governance/hg-intel-site`.

## Contents
- `index.html` — the page. Brand 2 (Colourful Lines / Streams): white canvas, blue→purple hero glow,
  animated regulatory/clinical/best-practice/privacy/funding "threads", cyber-blue gradient accents.
  Inline CSS, no external assets — opens standalone in any browser.
- `CNAME` — custom domain for GitHub Pages (`hg-intel.com.au`).

## Publish an update
Edit `index.html`, then:
```
git add -A && git commit -m "…" && git push
```
GitHub Pages rebuilds automatically (~1 min).

## Hosting / DNS
- **Pages:** build from `main`, root. Custom domain `hg-intel.com.au`, Enforce HTTPS on.
- **DNS (GoDaddy, domain stays registered there):** four apex `A` records →
  `185.199.108.153 / .109 / .110 / .111`; `www` `CNAME` → `holistic-governance.github.io`.
- **`hg-intel.com`** → 301 forward to `https://hg-intel.com.au` via GoDaddy Forwarding.

## Copy guardrails
Decision **support**, not legal/medical/clinical advice (carries the disclaimer). Names aged-care's
reset + **upcoming** NSQHS Standards — no fabricated dates. "Register your interest" → `info@hg-au.com`.

## Regenerate the preview (optional)
```
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu \
  --hide-scrollbars --force-device-scale-factor=2 --window-size=1280,1360 \
  --screenshot="preview.png" "file://$PWD/index.html"
```
