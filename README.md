# Armario — AI outfit app (mobile web)

**Status: clickable prototype (spec v0.6).** Nothing here calls an AI model yet. The camera, uploads, Google sign-in, clothing recognition, look generation, color palette and the scene chat are all simulated, and the photos are fixed AI-generated samples.

**Live:** https://juanpabloherrera.github.io/Outfitapp/

Designed for a phone screen of 402 × 874 pt (iPhone 18 Pro, still to be confirmed) and laid out to work from 375 to 440 pt wide. On a computer it shows inside a phone frame, with a side panel to jump to any screen and to simulate offline mode, a failed image and a rejected photo.

## What is in the repo

- `index.html` — the whole prototype: HTML, CSS and JS, no build step.
- `img/` — the sample images it uses.

## What is not built yet

GitHub Pages only serves static files, and everything it serves is public. The real app needs a backend for:

- recognizing clothing from photos,
- generating looks (2:3 portrait, Pinterest style) on the person's own photo,
- the color palette analysis,
- the scene chat agent,
- accounts and private photo storage.

The plan is to keep the front end static and put the AI calls and the photo storage behind a separate backend that holds the provider keys. Before building it, a fidelity test (does the generated look keep the real garment and the real person?) decides whether the product holds up.

## Rules for this repo

- **Never commit API keys or other secrets.** This repo is public. GitHub secret scanning with push protection is on, but it does not catch everything.
- **Never commit photos of real people or of their clothes.** User photos belong only in the private backend storage.
