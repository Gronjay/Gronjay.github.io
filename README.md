# Li Guangjie — Academic Website

A personal academic website built on [Academic Pages](https://github.com/academicpages/academicpages.github.io),
a Jekyll theme for GitHub Pages (a fork of Minimal Mistakes).

## What is inside

| Path | What it controls |
| --- | --- |
| `_config.yml` | Site title, author profile, sidebar, social links, collections |
| `_data/navigation.yml` | Top navigation menu |
| `_pages/about.md` | Home page |
| `_pages/research.md` | Research page |
| `_pages/cv.md` | CV page (Markdown + link to the PDF) |
| `_pages/publications.html` | Publications list (generated from `_publications/`) |
| `_publications/*.md` | One Markdown file per publication |
| `images/profile.jpg` | Sidebar avatar |
| `files/cv.pdf` | Downloadable CV PDF |
| `_sass/`, `assets/` | Theme styling and scripts — normally do not edit |

## Deploy on GitHub Pages (recommended)

1. Create a new **public** repository named `<your-github-username>.github.io`
   (for example `liguangjie.github.io`).
2. Upload this folder's contents to the repository (or push with git):
   ```bash
   git init
   git add .
   git commit -m "Initial academic website"
   git branch -M master
   git remote add origin https://github.com/<username>/<username>.github.io.git
   git push -u origin master
   ```
3. Open `_config.yml` and set `url` and `repository` to your own values:
   ```yaml
   url        : "https://<username>.github.io"
   repository : "<username>/<username>.github.io"
   ```
4. In the repository: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
5. Every push to `master` triggers `.github/workflows/jekyll.yml`, which builds the site and
   publishes it at `https://<username>.github.io` (usually within a minute or two).

## Preview locally

The site is plain Jekyll, so the canonical way is:

```bash
bundle install
bundle exec jekyll serve -l -H localhost
# open http://localhost:4000
```

If you do not want to install Ruby, open `../preview/index.html` in a browser — it is a static
snapshot generated from the same content files.

## Editing content

* **Text pages** are Markdown with a YAML front matter block at the top. Keep the `---` lines and
  the `permalink` value.
* **A new publication**: add a file such as `_publications/2026-06-01-my-paper.md` with
  `title`, `collection: publications`, `category: manuscripts`, `permalink`, `date`, `venue`,
  `excerpt`, `citation` and optionally `paperurl`.
* **A new publication category**: define it under `publication_category` in `_config.yml`.
* **Photos and PDFs**: put images in `images/`, PDFs in `files/`, then link to `/files/name.pdf`.
