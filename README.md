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
- `.github/workflows/deploy-pages.yml` deploys the site to GitHub Pages automatically on every push to `master`.

## GitHub Pages Setup

1. Push this repo to GitHub:

```bash
git push origin master
```

2. In the GitHub repo, open `Settings` -> `Pages`.

3. Under `Build and deployment`, set:
- `Source`: `GitHub Actions`

4. Wait for the `Deploy GitHub Pages` workflow to run once under the `Actions` tab.

5. In `Settings` -> `Pages`, set the custom domain to:
- `nebulacollective.org`

6. At your DNS provider, create these records for the apex/root domain:
- `A` -> `185.199.108.153`
- `A` -> `185.199.109.153`
- `A` -> `185.199.110.153`
- `A` -> `185.199.111.153`

7. Add `www` as a subdomain:
- `CNAME` -> `shawnj609.github.io`

8. After DNS resolves, go back to `Settings` -> `Pages` and enable `Enforce HTTPS`.

## Notes

- The workflow only publishes the actual site files, not the `workshop/` source material.
- DNS changes can take time to propagate; GitHub will not issue the TLS certificate until the domain points correctly.
