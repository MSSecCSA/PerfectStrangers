# Blog Setup Guide 🚀

Your collaborative blog is ready! Here's how to get it live on GitHub Pages.

## What's Been Built

✅ **Complete Hugo blog** with DarkPixelTech-inspired minimal design  
✅ **Custom dark theme** with blue accent color (easily customizable)  
✅ **Sample welcome post** demonstrating collaborative authorship  
✅ **GitHub Actions** for automatic deployment  
✅ **Git repository** initialized and ready to push  
✅ **Responsive design** that works on all devices  
✅ **Fast loading** with clean, semantic HTML  

## Quick Start (5 minutes)

### 1. Create GitHub Repository

```bash
# In the blog-site directory:
gh repo create blog-site --public --source=. --push
```

**OR manually:**
1. Go to GitHub.com → New Repository
2. Name it `blog-site` (or whatever you prefer)
3. Make it **public** (required for free GitHub Pages)
4. Don't initialize with README (we already have one)

### 2. Connect & Push

```bash
# Add GitHub as remote (replace USERNAME with your GitHub username)
git remote add origin https://github.com/USERNAME/blog-site.git

# Push everything
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repo on GitHub
2. **Settings** → **Pages** (in sidebar)
3. **Source**: Deploy from a branch → **GitHub Actions**
4. Wait 2-3 minutes for first deployment

Your blog will be live at: `https://USERNAME.github.io/blog-site/`

## Customization

### Change Colors

Edit `themes/minimal-dark/static/css/style.css`:

```css
:root {
    --accent-color: #2563eb;  /* Change this to any color */
}
```

Popular alternatives:
- `#16a34a` (green)
- `#dc2626` (red) 
- `#7c3aed` (purple)
- `#ea580c` (orange)

### Update Site Info

Edit `hugo.toml`:

```toml
baseURL = "https://USERNAME.github.io/blog-site/"  # Update this
title = "Your Blog Title"
[params]
  description = "Your blog description"
  author = "Your Name(s)"
```

### Add Custom Domain (Optional)

1. Buy domain from any registrar
2. Add CNAME record pointing to `USERNAME.github.io`
3. In GitHub repo: Settings → Pages → Custom domain
4. Update `baseURL` in `hugo.toml`

## Writing Workflow

### New Post

```bash
# Create new post
hugo new content posts/my-new-post.md

# Edit the file, then...
git add .
git commit -m "Add: My New Post"
git push
```

### Collaborative Review Process

```bash
# Create feature branch
git checkout -b post/article-name

# Write and edit
# When ready for review...
git add .
git commit -m "Draft: Article Title"
git push origin post/article-name

# Create pull request on GitHub
# Review together
# Merge when ready → auto-deploys
```

## Content Templates

### Blog Post Template

```markdown
---
title: "Your Post Title"
date: 2026-02-07T08:00:00Z
authors: ["Ben", "Daniel"]  # or ["Ben"] or ["Daniel"]
tags: ["ai", "development", "collaboration"]
draft: false
---

Brief summary that appears in post lists.

<!--more-->

Full content starts here...

## Section Headers

Use markdown as normal. Images, code blocks, links all work perfectly.

```python
# Code syntax highlighting works
def hello_world():
    return "Hello, collaborative world!"
```

Remember: every post represents our shared perspective.
```

## Maintenance

### Update Hugo (when needed)

```bash
# Check current version
hugo version

# Download latest from GitHub releases
# Replace existing binary in /usr/local/bin/
```

### Backup

Your content is safe in Git, but consider:
- Regular `git push` (obviously)
- Export content: `hugo --destination backup/`

## Troubleshooting

**Build fails?**
- Check GitHub Actions tab in repo
- Verify all files committed: `git status`
- Test locally: `hugo server`

**Site not updating?**
- Check Actions tab for deployment status
- Clear browser cache (Ctrl+F5)
- Wait 5 minutes for CDN propagation

**Styling issues?**
- Test locally first: `hugo server`
- Check browser console for errors
- Verify CSS path in baseof.html

## What's Next?

1. **Push to GitHub** (follow steps above)
2. **Customize colors** to your preference  
3. **Write your first real post** together
4. **Set up analytics** (Google Analytics 4, optional)
5. **Add comments** (Utterances with GitHub, optional)

## File Structure Reference

```
blog-site/
├── .github/workflows/    # Auto-deployment
├── content/
│   ├── posts/           # Your blog posts
│   └── about.md         # About page
├── themes/minimal-dark/ # Custom theme
├── hugo.toml           # Site configuration
├── README.md           # Documentation
└── SETUP_GUIDE.md      # This file
```

---

**Total setup time:** ~5 minutes  
**Total cost:** $0 (free GitHub Pages hosting)  
**Maintenance:** Minimal (Hugo + Git)

Ready to make it live? Run the GitHub commands above! 🎉

*Questions? Check the built-in README.md or create an issue in the repo.*