# khoatdvo.github.io

A minimal static site for serving files via GitHub Pages at the root domain.

**Live URL:** https://khoatdvo.github.io/

## Serving files

Put files under `files/` (or anywhere in the repo). Once deployed they're reachable at:

```
https://khoatdvo.github.io/files/<filename>
```

The landing page (`index.html`) links to whatever you list there. `.nojekyll`
is present so GitHub serves files as-is without Jekyll processing.

## Root-path serving

Because this repo is named `khoatdvo.github.io` (a GitHub "user site"), it is
served at the domain root with no `/<repo>/` path prefix. Any other repo name
would serve under `https://khoatdvo.github.io/<repo>/` instead.

## Deploying

A GitHub Actions workflow (`.github/workflows/deploy.yml`) publishes the repo
to Pages on every push to `main`.

**One-time setup:** in the repo on GitHub, go to
**Settings → Pages → Build and deployment → Source** and select
**GitHub Actions**.

Then push:

```bash
git add -A
git commit -m "Update static page"
git push origin main
```
