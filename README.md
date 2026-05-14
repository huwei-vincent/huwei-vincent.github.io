# HU Wei 胡维 — Personal Homepage

[![Website](https://img.shields.io/badge/website-huwei--vincent.com-blue)](https://huwei-vincent.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> Personal academic homepage of **HU Wei (胡维)**, Distinguished Research Fellow at the School of Economics and Management, Tongji University.

## Overview

This repository hosts the source code for my personal academic website, built with [Jekyll](https://jekyllrb.com/) and based on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) / [AcademicPages](https://github.com/academicpages/academicpages.github.io) theme. The site is deployed via [GitHub Pages](https://pages.github.com/) and served at [huwei-vincent.com](https://huwei-vincent.com).

## Site Structure

| Page | Description |
|------|-------------|
| [Home / About](https://huwei-vincent.com/) | English bio, education, and research interests |
| [关于我 (CN)](https://huwei-vincent.com/about-cn/) | Chinese version of the about page |
| [Research](https://huwei-vincent.com/my-publication/) | Publications and working papers |
| [Teaching](https://huwei-vincent.com/teaching/) | Courses taught at Tongji University |
| [Experiences](https://huwei-vincent.com/experiences/) | Academic and professional experiences |
| [Services](https://huwei-vincent.com/services/) | Academic services (reviewer, committee, etc.) |
| [Awards](https://huwei-vincent.com/awards/) | Honors and awards |
| [CV](https://huwei-vincent.com/cv/) | Curriculum vitae |
| [Blog](https://vincent27hugh.github.io/) | External blog link |

## Tech Stack

- **Static Site Generator**: [Jekyll](https://jekyllrb.com/)
- **Theme**: Minimal Mistakes / AcademicPages
- **Hosting**: GitHub Pages
- **Domain**: Custom domain via CNAME (`huwei-vincent.com`)
- **Styling**: SCSS / Sass
- **Plugins**: `jekyll-paginate`, `jekyll-sitemap`, `jekyll-feed`, `jekyll-gist`, `jekyll-redirect-from`

## Local Development

### Prerequisites

- Ruby >= 2.5
- Bundler

### Setup

```bash
# Clone the repository
git clone https://github.com/huwei-vincent/huwei-vincent.github.io.git
cd huwei-vincent.github.io

# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Or use the development config
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

The site will be available at `http://localhost:4000`.

## Project Structure

```
.
├── _config.yml              # Site configuration
├── _config.dev.yml          # Development overrides
├── _data/
│   ├── navigation.yml       # Top navigation menu
│   └── authors.yml          # Author metadata
├── _includes/               # Jekyll includes (header, footer, etc.)
├── _layouts/                # Page layouts
├── _pages/                  # Static pages (about, cv, teaching, etc.)
├── _posts/                  # Blog posts
├── _publications/           # Publication entries
├── _teaching/               # Teaching portfolio entries
├── _talks/                  # Talk / presentation entries
├── _portfolio/              # Portfolio items
├── assets/
│   ├── css/                 # Stylesheets
│   ├── js/                  # JavaScript
│   └── fonts/               # Icon fonts
├── files/                   # Downloadable files (CV PDFs)
├── images/                  # Images and favicons
├── markdown_generator/      # Python scripts to generate markdown from TSV/Bib
├── talkmap/                 # Leaflet map for talks
└── README.md                # This file
```

## Key Features

- **Bilingual support**: English and Chinese pages
- **Responsive design**: Mobile-friendly layout
- **Academic profiles**: Integrated links to Google Scholar, ORCID, ResearchGate, LinkedIn, and GitHub
- **Publication list**: Organized markdown-based publication management
- **Talk map**: Leaflet-based map visualization for academic talks
- **SEO ready**: Open Graph, Twitter Cards, and sitemap support

## Updating Content

Most site content is written in Markdown under the `_pages/` directory. To update:

- **Bio / About**: Edit `_pages/about.md` (EN) or `_pages/about-cn.md` (CN)
- **Publications**: Edit `_pages/my-publication.md` or use scripts in `markdown_generator/`
- **Teaching**: Add/modify files in `_teaching/`
- **Navigation**: Edit `_data/navigation.yml`
- **Site config**: Edit `_config.yml`

## License

This project is based on the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) theme by Michael Rose, licensed under the [MIT License](LICENSE).

## Contact

- Email: [huwei72@tongji.edu.cn](mailto:huwei72@tongji.edu.cn)
- GitHub: [@huwei-vincent](https://github.com/huwei-vincent)
- Google Scholar: [Profile](https://scholar.google.com/citations?hl=en&user=6CJRiM8AAAAJ)
