# Massimiliano Fanciulli — CV site (Jekyll)

Static personal site built with Jekyll, generated from a CV. Content lives in
`_data/*.yml`, so you can edit your experience, skills, projects, education,
certifications and languages without touching any HTML.

## Project structure

```
_config.yml          site settings (title, contact links, url/baseurl)
_layouts/default.html    page shell: <head>, nav, footer
index.html            homepage content, loops over the data files below
_data/experience.yml   work history (timeline)
_data/skills.yml       skills panel
_data/projects.yml     personal projects / open source
_data/education.yml
_data/certifications.yml
_data/languages.yml
assets/css/style.css
assets/js/main.js
```

## Run locally

Requires Ruby (3.x) and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000

## Editing content

Everything under `_data/` is plain YAML — add, remove or reorder entries and
the page updates automatically. Contact details, site title/description and
the deploy URL live in `_config.yml`.

## Deploying

### Option A — GitHub Pages (recommended, zero build step to maintain)

1. Push this repo to GitHub.
2. In the repo's **Settings → Pages**, set the source to **GitHub Actions**
   (the included workflow at `.github/workflows/pages.yml` builds and deploys
   on every push to `main`).
3. In `_config.yml`, set `url` to your Pages URL
   (e.g. `https://<username>.github.io`) and `baseurl` to `""` for a user/org
   site, or `"/<repo-name>"` for a project site.

Alternatively, GitHub Pages can build the site for you automatically without
the workflow file — just set the Pages source to the `main` branch — since
this repo only uses `github-pages`-approved plugins.

### Option B — Netlify / Vercel / any static host

Build command: `bundle exec jekyll build`
Publish directory: `_site`

## License / content

All content is Massimiliano Fanciulli's own CV data. Replace it with your own
by editing `_data/*.yml` and `_config.yml`.
