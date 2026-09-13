# shinnosukeono.github.io

Personal academic site for Shinnosuke Ono, built on the al-folio Jekyll theme. It supports
his PhD applications, so the home page should let a reader see in a few seconds what he
works on, what he has published, and where to find the CV.

## Where content lives

- `_pages/about.md` — home page: bio, and toggles for news, selected papers, social icons
- `_bibliography/papers.bib` — publications. `selected={true}` puts an entry on the home page.
  Supported extra fields include `abbr`, `preview`, `arxiv`, `code`, `supp`, `website`,
  `slides`, `poster`, `additional_info`, `award`.
- `_data/venues.yml` — colour and link for each `abbr`
- `_news/*.md` — one file per item, `inline: true`, sorted by `date`
- `_projects/*.md` — `category: research` or `category: talks`; `importance` sets the order
- `_data/cv.yml` — the rendered CV page; `uploads/resume.pdf` is the download
- `_config.yml` — site metadata, socials, scholar name matching

## Conventions

- The CV PDF is generated from `~/univ/00_projects/202604_us_phd_app/_共通/resume/resume.tex`.
  `_data/cv.yml` duplicates its content; change both together.
- Write project pages as question first, then what was done, then what came out. Keep them
  to a few paragraphs and link out rather than explaining at length.
- Never add a publication, award, or affiliation that is not already in the CV.

## Build

Local preview needs Docker; the `Dockerfile` pins `ruby:3.3` because upstream's
`ruby:latest` is currently broken.

```bash
docker build -t alfolio-local .
docker run --rm -v "$PWD":/srv/jekyll -w /srv/jekyll alfolio-local bundle exec jekyll build
```

Pushing to `master` deploys via `.github/workflows/deploy.yml` (GitHub Pages, Actions
artifact — the repository's Pages source is already set to "GitHub Actions").
