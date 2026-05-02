# YOUSSEF JAD | THE DIGITAL PORTER

> Delivering Solutions • One Strand at a Time

Welcome to the source code for my technical blog and digital persona. This platform is built to be a living document of my journey through software engineering, technical leadership, project management, and life itself. 

The site utilizes a custom-built, cinematic, dark-mode aesthetic heavily inspired by Hideo Kojima's *Death Stranding*. It emphasizes precision, readability, and a deep sense of atmosphere using carefully selected typography (Cinzel & Inter), "Chiral Gold" accents, and "Frost Blue" interactive elements.

## 🏗️ Technology Stack

- **Static Site Generator:** [Hugo](https://gohugo.io/)
- **Styling:** Custom CSS (Cinematic Dark Mode, Glassmorphism UI)
- **Environment:** Containerized via Docker (`hugomods/hugo:exts`)
- **Workflow Automation:** Make (`Makefile`)
- **Hosting:** GitHub Pages (`youssef-jad.github.io`)

---

## 🚀 Local Development

You do not need Hugo installed locally on your machine. Everything runs securely through Docker via simple Make commands.

To spin up the local development server with hot-reloading:

```bash
make dev
```
The site will be available at `http://localhost:1313`.

---

## 📦 Building & Deploying

To compile the site for production and publish the changes to GitHub Pages, follow this workflow:

1. **Build the static site:**
   ```bash
   make build-site
   ```
   *This compiles all Markdown/HTML files and dumps the highly-optimized output into the `public/` directory.*

2. **Deploy to GitHub:**
   Navigate into the `public` directory and push your changes:
   ```bash
   cd public
   git add .
   git commit -m "Deploying latest articles"
   git push -u origin main -f
   ```

*(Note: We are planning to automate the deployment step via GitHub Actions in the future).*

---

## ✒️ Content Architecture

Content is primarily placed in `/content/posts/` and is written in HTML/Markdown. 

To maintain the **Digital Porter** cinematic aesthetic, articles should utilize the centralized design tokens located in our global CSS pipeline rather than inline styles. 

**Core Components for Articles:**
- **Callouts:** Use `<div class="callout warning">`, `<div class="callout success">`, or `<div class="callout danger">` for critical information.
- **Rules Grids:** Use `<div class="rules-grid">` to display side-by-side comparative matrices.
- **Tags:** Use the custom `<div class="tag-row">` block at the top of articles to label content (e.g., *Tech Lead*, *Engineering*, *Personal*).
- **Code Blocks:** Wrap terminal/code snippets in standard `<pre><code>` blocks. The centralized theme will automatically apply dark-mode syntax highlighting.

---

*"I'll keep on keeping on."*
