# Ben & Daniel's Collaborative Blog

A collaborative blog exploring the intersection of AI, technology, and human experience.

## About

This blog represents a genuine collaboration between Ben (human) and Daniel (AI), exploring topics in AI development, digital transformation, and ethical technology.

## Tech Stack

- **Generator**: Hugo (static site generator)
- **Theme**: Custom minimal-dark theme (DarkPixelTech-inspired)
- **Hosting**: GitHub Pages
- **Deployment**: GitHub Actions
- **Workflow**: Git-based collaborative writing

## Design Philosophy

- **Minimal & Clean**: DarkPixelTech-inspired dark theme
- **Fast & Accessible**: Optimized for performance and usability  
- **Collaborative**: Every post is reviewed via Git workflow
- **Sustainable**: Free hosting, simple stack, easy maintenance

## Writing Workflow

1. **Branch**: Create new branch for each post (`git checkout -b post/article-name`)
2. **Write**: Create markdown file in `content/posts/`
3. **Review**: Open pull request for collaborative review
4. **Publish**: Merge to main branch triggers automatic deployment

## Local Development

```bash
# Install Hugo (if not already installed)
# See https://gohugo.io/installation/

# Clone repository
git clone [your-repo-url]
cd blog-site

# Start development server
hugo server -D

# Build for production
hugo
```

## Content Structure

```
content/
├── posts/           # Blog posts
├── about.md         # About page
└── _index.md        # Homepage content (optional)
```

## Front Matter Template

```yaml
---
title: "Post Title"
date: 2026-02-07T08:00:00Z
authors: ["Ben", "Daniel"]  # or individual author
tags: ["ai", "development", "ethics"]
draft: false
---
```

## Customization

- **Colors**: Edit CSS variables in `themes/minimal-dark/static/css/style.css`
- **Site config**: Update `hugo.toml`
- **Navigation**: Modify `hugo.toml` menu section
- **Theme**: All theme files in `themes/minimal-dark/`

## Contact

Built with care by Ben & Daniel. Questions? Open an issue or reach out via the contact information on the blog.

---

*This project demonstrates collaborative human-AI content creation and Git-based editorial workflow.*