# Tabaq – One Year Anniversary Website

A scroll-driven romantic story website (pastel sunset sky, fluffy pink clouds, real pink lilies).
Everything is in a single self-contained `index.html` (images are embedded), so you can just open it
in a browser or host it anywhere (GitHub Pages, Vercel, Netlify).

## Sections (in scroll order)
1. **Hero** – `HAPPY ONE YEAR MERII PIYARI SI TABAQQ` on a sunset sky with lilies and bubbles
2. **Cloud fly-through → Message card** – the Roman Urdu message, revealed word by word, with a cat walking on the card
3. **Photo album (oval frame)** – photo 1 → photo 3 → photo 2, with a bloom transition between them
4. **Floating book** – opens as you scroll; note: `MERII JAN / AP MERA SA APNI BOOK LAI LAIN`
5. **Sunset surprise** – gold heart → sun window → `Take your surprise` → `I took it 💍` (ring, confetti, final message)

## Tech
GSAP + ScrollTrigger + Lenis (loaded from CDN) for the scroll-scrubbed animation. No build step.

## Editing
- **Photos:** in `index.html` search for `var A={` – the keys `p1`, `p2`, `p3` hold the album photos (base64).
  The album order is set in the `list=[...]` array (currently p1, p3, p2).
- **Texts:** search for the Roman Urdu strings (`MERA LIA MERII JAN ...`, `MERA SAB HAIN AP OR HAMESHA RAHAIN GI`).
- **Timeline:** the `tl.to(...)/tl.fromTo(...)` calls; the last argument is the position on the scroll timeline.
