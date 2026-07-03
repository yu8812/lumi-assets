# lumi-assets

Static media for the [Lumi TOEIC platform](https://github.com/yu8812/lumi).
Served globally via [jsDelivr](https://www.jsdelivr.com/) CDN.

## License / usage

**Copyright (c) Lumi. All rights reserved.**

This repository is public **only** because jsDelivr requires a public
GitHub repo to serve files. Public visibility is not a license grant:
the audio recordings, images, and audiobook media here are original
works created for the Lumi platform. You may not copy, redistribute,
rehost, or use them in another product or dataset without written
permission. Hotlinking outside the Lumi app is not permitted.

## Why a separate repo?

The main `lumi` repo holds only code so clones stay fast. Audio files (~16K
mp3s, ~170MB) and Part 1 photographs live here and are fetched at runtime via:

```
https://cdn.jsdelivr.net/gh/yu8812/lumi-assets@main/audio/...
https://cdn.jsdelivr.net/gh/yu8812/lumi-assets@main/images/...
```

## Layout

- `audio/vocab/<word>-<accent>.mp3` — vocabulary pronunciations (us / gb / au / ca)
- `audio/part1/`, `audio/part2/`, `audio/part3/`, `audio/part4/` — TOEIC Listening
- `images/part1/` — Part 1 photograph descriptions

## Updating

Push to this repo's default branch. jsDelivr caches for ~12 hours; for instant
updates use a versioned tag (`@v2` etc.) and bump `PUBLIC_ASSET_BASE_URL` in
the main app.

## License

Audio synthesized via Azure Neural TTS. Images generated via Pollinations.AI
(Flux models). Use is for educational TOEIC practice within the Lumi platform.
