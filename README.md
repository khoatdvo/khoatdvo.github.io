# static-page

A minimal static site for serving files via GitHub Pages.

**Live URL:** https://khoatdvo.github.io/static-page/

## Serving files

Put files under `files/` (or anywhere in the repo). Once deployed they're reachable at:

```
https://khoatdvo.github.io/static-page/files/<filename>
```

The landing page (`index.html`) links to whatever you list there. `.nojekyll`
is present so GitHub serves files as-is without Jekyll processing.

## Deploying

A GitHub Actions workflow (`.github/workflows/deploy.yml`) publishes the repo
to Pages on every push to `main`.

**One-time setup:** in the repo on GitHub, go to
**Settings → Pages → Build and deployment → Source** and select
**GitHub Actions**.

Then push:

```bash
git add -A
git commit -m "Init static page"
git push -u origin main
```
