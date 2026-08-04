# Sombuilder Online

Marketing site for **Sombuilder Online** — scalable full-stack platforms, offline-first PWAs, and custom enterprise CRM systems.

A single, fully self-contained page: React, ReactDOM, and all Tailwind CSS are precompiled and inlined directly into `index.html`. There's no build step, no CDN dependency, and no network access required to run it — open the file and it works, even offline.

## Run locally

No build step needed. Either:

- Open `index.html` directly in a browser, or
- Serve it locally so relative paths and PWA behavior work as expected:

```bash
npx serve .
# or
python3 -m http.server 8080
```

Then visit `http://localhost:8080` (or whatever port your tool prints).

## Deploy to GitHub Pages

This repo includes a workflow at `.github/workflows/deploy.yml` that publishes the site automatically.

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **GitHub Actions**.
4. Push to `main` (or run the workflow manually from the **Actions** tab).

Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

### Alternative: deploy without the workflow

If you'd rather not use Actions, go to **Settings → Pages → Source** and choose **Deploy from a branch**, then pick `main` and the `/ (root)` folder. GitHub will serve `index.html` directly — no workflow required.

## Deploy elsewhere

Since it's a static file, `index.html` also works as-is on Netlify, Vercel, Cloudflare Pages, or any static host — just point them at the repo root with no build command.

## Notes

- Fonts (Inter, JetBrains Mono) are still pulled from Google Fonts at runtime; everything else (React, ReactDOM, Tailwind's compiled CSS, and the app itself) is bundled inline with no external dependency.
- The `LICENSE` file is a placeholder MIT license — swap it out or remove it if you'd prefer different terms.
