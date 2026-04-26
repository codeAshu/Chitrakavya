# Chitrakāvya — research site

A static rebuild of the IIITB-CSL Chitrakāvya project archive, with fresh SVG illustrations, interactive demos, and validated knight's tours.

## Files

- `index.html` · landing
- `visuals.html` · bandhas gallery, sarvatōbhadra, **Modern English Chitrakāvya by Donald Knuth (2005)**, Modern Sanskrit Chitrakāvyas (1800–1900)
- `knights-tour.html` · Pādukāsahasra knight's-tour walk-through
- `resources.html` · bibliography
- `about.html` · project notes
- `assets/` · stylesheet, SVGs, audio (`poem1.mp3`, `poem2.mp3`)
- `vercel.json` · deploy config

## Deploy on Vercel

Two ways:

### One-line CLI

```bash
cd Chitrakavya
npx vercel deploy --prod
```

The CLI will ask you to log in and pick a scope; the static site needs no build step. Vercel auto-detects the `vercel.json` and serves the folder as-is.

### Git push (recommended)

1. Push this folder to a GitHub repo.
2. Open https://vercel.com/new and import the repo.
3. Framework preset: **Other** · Root directory: `Chitrakavya/` (or repo root if you push only this folder) · Build command: *(leave empty)* · Output directory: *(leave empty / `.`)*
4. Click **Deploy**. The default `vercel.json` is already in place.

The site is plain HTML+CSS+SVG+JS; total payload is well under 1 MB including audio.

## Audio

- `assets/poem1.mp3` — re-encoded from the IIITB Flash original (`Knuth poem.swf`).
- `assets/poem2.mp3` — re-encoded from `knuth-poem2.wav`.

If the browser blocks autoplay (Safari mobile, etc.), the page automatically falls back to the Web Speech API to recite the verses.

## Local preview

```bash
cd Chitrakavya
python3 -m http.server 8080
# open http://localhost:8080
```

## Credit

Visual chitrakāvya pairs and Sanskrit bandha figures redrawn from the IIITB-CSL
project archive. Knuth verses transcribed from the same archive (2005).
Knight's tours generated and verified at build time using Warnsdorff's heuristic
with backtracking.
