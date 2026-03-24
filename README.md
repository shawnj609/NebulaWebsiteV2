# Nebula Collective Website

Launchable static website for `Nebulacollective.org`, with content grounded in the provided nonprofit narrative and program documents.

## Pages

- `index.html` - Home
- `education.html` - Nebula Academy tracks, delivery, and yearly output targets
- `technology.html` - Toolchains, system scope, and safety boundaries
- `showcase.html` - Nebula Pop-Ups timeline and public-art delivery model
- `about.html` - Operations, funding model, and support information
- `experience.html` - End-to-end participant journey across programs
- `learn-more.html` - FAQ and program logistics summary

All navigation tabs and in-page CTAs are wired for click-through across pages.

## Run Locally

From the repo root:

```bash
python3 -m http.server 8080
```

Then open:

- [http://localhost:8080/index.html](http://localhost:8080/index.html)

## Hosting Notes

- `CNAME` is set to `Nebulacollective.org` for GitHub Pages style hosting.
- This is a static HTML + CSS site (`site.css`), so no Node install is required.
