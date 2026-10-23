# FRC Team Website Template

A Jekyll site meant to be forked/"Used as template" by any FRC team. Public link-tree homepage + scouting link, with three team-only sections (build logs, portal, materials) meant to sit behind Cloudflare Access.

## Make it yours

Edit **`_config.yml`** — that's the only file most teams need to touch:
- `team_number`, `team_name`, `title`, `tagline`
- `links` — the buttons on the homepage
- `brand_color` — hex color used throughout

## Run it locally (optional)

Requires Ruby. On your own machine (not this sandbox):

```
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000

You don't have to do this — pushing to GitHub and turning on GitHub Pages builds it for you automatically, no local install needed.

## Deploy

1. Push this repo to GitHub.
2. Repo Settings → Pages → set source to your default branch.
3. (Optional, for the private sections) Point a custom domain's DNS through Cloudflare, then add Cloudflare Access applications for `/build-logs/*`, `/portal/*`, `/materials/*`, restricted to your team's emails.

## Structure

```
_config.yml       ← team settings — edit this
index.md          ← public link tree (homepage)
scouting.md        ← public page linking to the external scouting app
build-logs/        ← team-only (gate with Cloudflare Access)
portal/            ← team-only (gate with Cloudflare Access)
materials/         ← team-only (gate with Cloudflare Access)
_layouts/          ← page templates
assets/css/        ← styling (edit style.scss)
```

## Make this a template for other teams

Once this works for your own team: repo **Settings → check "Template repository."** Other teams click "Use this template," edit `_config.yml`, and deploy.
