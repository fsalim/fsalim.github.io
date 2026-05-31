# Flora Salim — Academic Website

A single-page academic site (plain HTML + CSS, no build step) ready for GitHub Pages.

## Files

```
index.html                      # the whole site
.nojekyll                       # tells GitHub Pages to serve files as-is (no Jekyll)
images/
  Flora_profile.jpg             # sidebar portrait  (see note below)
  cruise_group_nov2025.jpeg     # CRUISE group photo
```

> **Profile photo:** the page loads `images/Flora_profile.jpg`. If you push to your
> existing `fsalim.github.io` repo, that file is already there. For a brand-new repo,
> copy your original `Flora_profile.jpg` into the `images/` folder. If it is missing,
> the page automatically falls back to the copy on your current live site.

## Quick start (recommended)

Double-click **`setup-github-pages.command`** (or run `bash setup-github-pages.command`).
It initialises the git repo and makes the first commit, then prints the two commands
to connect GitHub and push. After that:

```bash
git remote add origin https://github.com/fsalim/fsalim.github.io.git
git push -u origin main          # add --force if overwriting your old site
```

## Publish to GitHub Pages (manual)

### Option A — your personal site (`fsalim.github.io`)
This serves at `https://fsalim.github.io`.

```bash
git remote add origin https://github.com/fsalim/fsalim.github.io.git
git branch -M main
git push -u origin main
```

If the remote already has the old site, either push over it (above) or pull/merge first.
GitHub Pages for a `username.github.io` repo publishes automatically from `main`.

### Option B — a project repo (e.g. `website`)
Serves at `https://fsalim.github.io/website/`.

```bash
git remote add origin https://github.com/fsalim/website.git
git branch -M main
git push -u origin main
```

Then in the repo: **Settings → Pages → Build and deployment → Source: Deploy from a
branch → Branch: `main` / root → Save.**

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Editing

Everything (content + styling) lives in `index.html`. Search for a section id
(`#about`, `#research`, `#publications`, `#service`, `#awards`, `#talks`, `#team`,
`#contact`) to find and edit that block.
