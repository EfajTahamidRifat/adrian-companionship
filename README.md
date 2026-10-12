# Adrian · Companionship & Mental Fortitude

Animated one-page site for Adrian's in-person companionship and mental fortitude sessions ($150/hour, "I come to you").

## What's inside
- `index.html` — the whole site (inline CSS + JS). Libraries load from CDNs: GSAP 3.13 + ScrollTrigger, Lenis 1.1.14, Google Fonts.
- `frames/` — 150-frame hero sequence (30fps), scrubbed on scroll inside the arch.
- `about.webp`, `pola-*.webp`, `plate.webp` — photos and background plate.

## Run locally
Any static server works:
```
npx serve .
```

## Deploy
Static site, no build step. Import the repo in Vercel or Netlify and deploy as-is.

## Swap the frame sequence
```
ffmpeg -i clip.mp4 -vf "fps=30,scale=720:-2" -frames:v 150 frames/f%03d.webp
```
