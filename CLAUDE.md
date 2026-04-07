# Shinnosuke Ono's Portfolio Website

## Project Overview
This is a personal academic portfolio website for Shinnosuke Ono, built using the Hugo static site generator with the Wowchemy Academic theme (now Hugo Blox). The site is hosted on GitHub Pages at https://shinnosukeono.github.io/.

## Owner Information
- **Name**: Shinnosuke Ono
- **Role**: Master's Student (Second Year)
- **Institution**: University of Tokyo
- **Department**: Computer Science (supervised by Prof. Masashi Sugiyama and Prof. Takashi Ishida)
- **Additional Position**: Research Assistant at Matsuo-Iwasawa Lab
- **Research Interests**: Representation Learning, Multimodal Models, Language Models, Reinforcement Learning
- **Email**: ono-shinnosuke637@g.ecc.u-tokyo.ac.jp

## Technology Stack
- **Static Site Generator**: Hugo (v0.89.4)
- **Theme**: Hugo Blox (formerly Wowchemy Academic)
- **Language**: Go modules (go 1.19)
- **Deployment**: Netlify (with netlify.toml configuration)
- **Version Control**: Git (repository on GitHub)

## Project Structure
```
shinnosukeono.github.io/
├── config/               # Hugo configuration files
│   └── _default/
│       ├── config.yaml   # Main Hugo configuration
│       ├── languages.yaml
│       ├── menus.yaml
│       └── params.yaml
├── content/              # Main content directory
│   ├── authors/
│   │   └── admin/       # Profile information
│   ├── home/            # Homepage sections
│   ├── post/            # Blog posts
│   ├── publication/     # Academic publications
│   ├── project/         # Research projects
│   └── poster/          # Academic posters
├── assets/              # Style and asset files
│   ├── scss/            # Custom styling
│   └── media/           # Images and icons
├── layouts/             # Custom Hugo layouts
├── static/              # Static files
│   └── uploads/         # PDF uploads (CV, resume)
├── public/              # Generated site (output)
├── data/                # Data files for themes and sharing
├── i18n/                # Internationalization
├── go.mod               # Go module dependencies
├── netlify.toml         # Netlify deployment config
└── my_library.bib       # Bibliography file
```

## Key Features
1. **Academic Profile**: Comprehensive academic CV with education, research interests, and social links
2. **Publications**: Structured publication entries with metadata, abstracts, and links
3. **Projects**: Research project showcases
4. **Blog Posts**: Technical blog posts about various topics
5. **Posters**: Academic poster presentations
6. **Multi-language Support**: Configured for English (primary)
7. **SEO Optimized**: With Hugo Blox SEO module

## Recent Publications (Example)
- **"A Japanese Language Model and Three New Evaluation Benchmarks for Pharmaceutical NLP"** (2025)
  - Authors: Issey Sukeda, Takuro Fujii, Kosei Buma, Shunsuke Sasaki, Shinnosuke Ono
  - Published as arXiv preprint
  - Includes links to PDF, code, dataset, and model

## Development Commands
```bash
# Local development server
hugo server

# Build site
hugo --gc --minify

# Build with future posts
hugo --gc --minify --buildFuture

# Deploy (handled by Netlify automatically)
```

## Important Files to Edit
1. **Profile**: `content/authors/admin/_index.md`
2. **Publications**: `content/publication/*/index.md`
3. **Blog Posts**: `content/post/*/index.md`
4. **Homepage Sections**: `content/home/*.md`
5. **Configuration**: `config/_default/*.yaml`
6. **Custom Styles**: `assets/scss/custom.scss`

## Git Information
- **Current Branch**: master
- **Main Branch**: master
- **Recent Commits**: Updates to workflow, build actions, and content

## Deployment
The site is automatically deployed via GitHub Pages when changes are pushed to the master branch. The site uses GitHub Actions for the build process (based on recent commits mentioning "add build actions").

## Notes for Future Development
1. The CV/resume PDF is stored at `static/uploads/resume.pdf`
2. Custom layouts are used for publications and other content types
3. The site uses Hugo's taxonomy system for tags, categories, and publication types
4. LaTeX math support is enabled via MathJax
5. The site supports both light and dark themes

## Maintenance Tasks
- Regular updates to publications and projects
- Keeping Hugo and theme modules updated
- Updating CV/resume PDF
- Adding new blog posts or research updates
- Monitoring build status on GitHub Actions