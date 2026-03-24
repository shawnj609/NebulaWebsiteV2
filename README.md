# Nebula Collective Website

Launchable static website prototype for `Nebulacollective.org`, assembled from the design workshop prototypes in [`workshop/`](./workshop).

## Pages

- `index.html` - Home
- `showcase.html` - Public shows + gallery
- `technology.html` - Production technology
- `education.html` - Workshops + curriculum
- `about.html` - Mission, legal anchors, support
- `experience.html` - Placeholder destination for hero CTA
- `learn-more.html` - Placeholder destination for hero CTA

All top navigation tabs are wired for click-through across pages.

## Run Locally

From the repo root:

```bash
python3 -m http.server 8080
```

Then open:

- [http://localhost:8080/index.html](http://localhost:8080/index.html)

## Hosting Notes

- `CNAME` is set to `Nebulacollective.org` for GitHub Pages style hosting.
- This is currently a static HTML/Tailwind-CDN build, so no Node install is required.
