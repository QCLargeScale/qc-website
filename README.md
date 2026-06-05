# QCLS — qc-website

**Hybrid solutions for scientific computing.**

The website for the QCLS project. It's built with [Zensical](https://zensical.org/)
(the successor to Material for MkDocs) and deployed automatically to GitHub Pages.

🌐 **Live site:** <https://qclargescale.github.io/qc-website/>

## Sections

- **Project** — overview and references
- **Objectives**
- **Project Plan**
- **Presentations**
- **Publications**

## Building the site locally

Tested with Python 3.13, but 3.10+ works.

```bash
# create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# install dependencies
pip install -r requirements.txt

# live preview with auto-reload at http://localhost:8000
zensical serve

# or produce a static build into the site/ directory
zensical build
```

Before pushing, run the same check CI runs — if it builds locally, it builds in CI:

```bash
zensical build --clean
```

`No issues found` means you're good to go. To do the check and push in one go, so a
broken build never reaches GitHub:

```bash
zensical build --clean && git add . && git commit -m "your message" && git push
```

## Project layout

```
.
├─ docs/                 # content (Markdown) + assets, figures, stylesheets
├─ overrides/
│  └─ main.html          # theme override: adds the ARIS sponsor logo to the footer
├─ mkdocs.yml            # site configuration (Zensical reads this)
├─ requirements.txt      # just: zensical
└─ .github/workflows/
   └─ deploy.yml         # build + deploy to GitHub Pages
```

### Theme customization

The footer sponsor logo comes from `overrides/main.html`, which extends the base
template and adds a sponsor bar. The config points at it via `theme.custom_dir: overrides`.
Zensical honors this override, so the customization works as-is — leave `overrides/` in place.

## Editing

1. Edit or add a `.md` file under `docs/`.
2. Add new pages to the `nav:` section of `mkdocs.yml` so they appear in the navigation.
3. Preview with `zensical serve`, then commit and push.

> **Note:** Reference/citation labels like `[2]` at the start of a line must be escaped
> (`\[2\]`) — otherwise Zensical reads them as empty links and warns. They render the same.

## Deployment

Deployment is **automatic**. Every push to `main` triggers the GitHub Actions workflow in
`.github/workflows/deploy.yml`, which checks the required files, builds the site with
Zensical, and publishes it to GitHub Pages. Pull requests run the check and build steps as
validation but do not deploy. You can watch a run under the repository's **Actions** tab.

## Funding & licence

© 2026 Ezhilmathi Krishnasamy · Funded by ARIS (Grant No. ARIS-RZK-2025/54).
