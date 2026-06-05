# Migrating the qc-website (QCLS) to Zensical

Tested with zensical 0.0.44 — the full site (8 pages) builds with **"No issues found"**,
and your custom footer override (the ARIS sponsor logo) renders correctly.

## Good news: this was a light migration

Your config was already mostly Zensical-ready — the only plugin is `search`, and all your
Markdown extensions are standard/supported. Most importantly, **Zensical honored your
template override**: `overrides/main.html` (the `{% extends "base.html" %}` footer block
with the sponsor logo) works, so `theme.custom_dir: overrides` is kept as-is.

## Files to add / replace

| File                           | Action                                            |
| ------------------------------ | ------------------------------------------------- |
| `mkdocs.yml`                   | **Replace** — two small fixes (below).            |
| `docs/index.md`                | **Replace** — bibliography brackets escaped.      |
| `requirements.txt`             | **Add** — there wasn't one; now just `zensical`.  |
| `.github/workflows/deploy.yml` | **Add** — Zensical build + GitHub Pages deploy.   |

`overrides/main.html` is unchanged — keep it. All your `docs/` content, figures, and
stylesheets stay as-is.

## Files to delete

- `setup.sh` — it ran `mkdocs gh-deploy`; deployment is now the Actions workflow.

## What changed

- **Removed `favicon: assets/favicon.png`** from the theme config — that file doesn't
  exist in the repo (dangling reference). If you want a custom favicon, add the file and
  restore the line: `favicon: assets/favicon.png`.
- **`repo_url`**: dropped the trailing `.git` (`.../qc-website.git` → `.../qc-website`).
- **`docs/index.md`**: escaped the leading brackets in the References section
  (`[2] …` → `\[2\] …`, etc.). They render exactly the same — the brackets still show —
  but Zensical no longer reads them as empty link references. This was the source of all
  11 build warnings.
- **Theme, plugins, extensions, palette, fonts, and the `overrides/` template are unchanged.**

## Build & preview locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

zensical serve     # preview at http://localhost:8000
zensical build     # static build into site/
```

## Deployment switch

You deployed with `mkdocs gh-deploy` (a `gh-pages` branch). The new workflow uses GitHub
Actions, so in the repo go to **Settings → Pages → Source** and select **GitHub Actions**.
Once a deploy succeeds, you can delete the old `gh-pages` branch.

## Note on future content

A few pages exist that aren't in the `nav:` (`about.md`, `docs.md`) — Zensical builds them
as standalone pages reachable by URL but not shown in navigation, same as MkDocs did. Add
them to `nav:` if you want them linked, or move them out of `docs/` if they shouldn't be
published.
