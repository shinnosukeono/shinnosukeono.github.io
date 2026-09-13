# shinnosukeono.github.io

Personal academic site, built with [al-folio](https://github.com/alshedivat/al-folio)
(Jekyll). Deployed to GitHub Pages by `.github/workflows/deploy.yml` on every push to
`master`.

## Editing

| what                      | where                                      |
| ------------------------- | ------------------------------------------ |
| bio, home page            | `_pages/about.md`                          |
| publications              | `_bibliography/papers.bib`                 |
| venue badges              | `_data/venues.yml`                         |
| news items                | `_news/*.md` (one file each, `inline: true`) |
| research and talks        | `_projects/*.md` (`category: research` or `talks`) |
| CV page                   | `_data/cv.yml`                             |
| CV PDF                    | `uploads/resume.pdf`                    |
| site metadata, socials    | `_config.yml`                              |

The CV PDF is built from `~/univ/00_projects/202604_us_phd_app/_共通/resume/resume.tex`.
`_data/cv.yml` duplicates it, so update both.

A paper appears on the home page only if its BibTeX entry has `selected={true}`.

## Local preview

The upstream Docker image is built from `ruby:latest`, which currently breaks. This repo
pins `ruby:3.3` in the `Dockerfile`:

```bash
docker build -t alfolio-local .
docker run --rm -p 8080:8080 -v "$PWD":/srv/jekyll -w /srv/jekyll alfolio-local \
  bundle exec jekyll serve --host 0.0.0.0 --port 8080
```

## Upstream

`git remote` `alfolio` points at the template. To pull in upstream changes:

```bash
git fetch alfolio master && git merge alfolio/master
```
