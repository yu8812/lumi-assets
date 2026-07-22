# Tarot card faces — Rider-Waite-Smith (RWS), 1909

78 card images (`<card-id>.webp`, 500px wide) for Lumi's tarot draw tool.
File name = Lumi's stable card id (see `tarot-basics/content/tarot.ts`), e.g.
`major-00-fool.webp`, `wands-11-page.webp`, `pentacles-14-king.webp`.

## Provenance & licence (public domain)

- **Deck**: Rider-Waite-Smith Tarot. Illustrated by **Pamela Colman Smith**,
  directed by Arthur Edward Waite. First published **December 1909** by
  William Rider & Son, London.
- **Source scans**: Wikimedia Commons, category *"Rider-Waite tarot deck"*
  (majors `RWS_Tarot_NN_Name.jpg`; minors `Wands/Cups/Swords/Pents NN.jpg`).
- **Copyright status — public domain worldwide (as of 2026)**:
  - **US**: published 1909, i.e. before 1929 → `PD-US-expired`.
  - **UK/EU**: Pamela Colman Smith died **1951**; life + 70 years expired at
    the end of **2021**, so PD in the UK/EU from 2022 onward.
  Wikimedia hosts these as `{{PD-old}}` / `{{PD-US-expired}}`.

No rights reserved by Lumi over the artwork itself. The 1971 recoloured
"Rider" edition (US Games) is a *separate* copyrighted work and is **not**
used here — only the original 1909 plates.

## How they were produced

`scripts/fetch-tarot-rws.ts` (Lumi repo, one-off): fetch each card via
Wikimedia `Special:FilePath/<file>?width=600` → `sharp` resize to 500px
wide, WebP q82. Idempotent (re-run skips existing). Not part of CI.
