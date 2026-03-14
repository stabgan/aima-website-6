# AIMA Exercises Website (v6) — Jekyll Edition

A Jekyll-powered static site for browsing exercises from *Artificial Intelligence: A Modern Approach*. Features MathJax-rendered equations, Disqus commenting, and GitHub Pages deployment.

## What It Does

- Renders AIMA textbook exercises (Chapters 7 and 14) with full LaTeX math support
- Provides a blog-style layout with individual posts per exercise set
- Supports community discussion through Disqus comments
- Auto-generates sitemap and RSS feed via Jekyll plugins

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| 💎 [Jekyll](https://jekyllrb.com/) | Static site generator |
| 📐 [MathJax](https://www.mathjax.org/) | LaTeX math rendering |
| 💬 [Disqus](https://disqus.com/) | Comment system |
| 🚀 GitHub Pages | Hosting |
| 🎨 SCSS | Styling with Sass partials |

## Getting Started

### Prerequisites

- [Ruby](https://www.ruby-lang.org/) 2.5+
- [Jekyll](https://jekyllrb.com/docs/installation/) 3.x

### Local Development

```bash
git clone https://github.com/stabgan/aima-website-6.git
cd aima-website-6
gem install jekyll bundler
jekyll serve
```

Visit `http://localhost:4000/aima-website-6/`.

### Adding Exercises

1. Create a new `.md` file in `_posts/` with the naming convention `YYYY-M-D-Title.md`
2. Include front matter: `layout: post`, `title`, and `comments: true`
3. Write exercises using Markdown with LaTeX math (`$...$` for inline)

## Project Structure

```
├── _config.yml          # Jekyll site configuration
├── _includes/           # Reusable HTML partials (meta, disqus, icons)
├── _layouts/            # Page templates (default, page, post)
├── _posts/              # Exercise markdown files
├── _sass/               # SCSS partials
├── about.md             # About page
├── index.html           # Home page listing all posts
└── style.scss           # Main stylesheet
```

## ⚠️ Known Issues

- The Disqus shortname references the old GitHub username; comments from the original deployment may not carry over.
- Exercise cross-references (e.g., `Figure [name](#/)`) use placeholder anchors and do not resolve to actual figures.
- Some SVG images are hosted externally on `nalinc.github.io` and may become unavailable.
