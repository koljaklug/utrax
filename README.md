# utrax
U-Trax website 


# Personal Portfolio Website — v4

A lightweight, static professional portfolio site built for:

- Cloudflare Pages
- GitHub-based deployment
- Easy long-term maintenance
- Fast performance
- Minimal dependencies
- Simple future customization

This project intentionally avoids frameworks and build tooling so the site remains durable, portable, and easy to edit years from now.

---

# Philosophy

This site is designed around several principles:

## 1. Static First
No backend.
No database.
No JavaScript framework.

Advantages:
- extremely fast
- secure
- cheap/free hosting
- minimal maintenance
- long-term stability

---

## 2. Easy Future Editing

The structure is intentionally modular:

- reusable section patterns
- centralized CSS variables
- semantic HTML
- isolated layout blocks

This allows:
- visual redesigns without touching content
- content edits without breaking layout
- future migration into Astro/React if desired

---

## 3. Professional Minimalism

The site emphasizes:
- typography
- spacing
- hierarchy
- restrained visual design

The goal is clarity and professionalism rather than flashy UI.

---

# File Structure

```text
project-root/
├── index.html
├── style.css
├── README.md
├── resume.pdf
├── favicon.ico
├── images/
└── assets/
```

---

# Core Files

## index.html

Contains:
- site structure
- content
- semantic sections
- navigation
- metadata

This is the primary editable content file.

---

## style.css

Contains:
- design system
- typography
- layout
- responsive behavior
- color variables
- reusable utilities

All visual changes should happen here first.

---

# Design System

The CSS uses centralized variables at the top of `style.css`.

Example:

```css
:root {
  --color-bg: #0f1115;
  --color-primary: #7c9cff;
  --text-xl: 2.5rem;
}
```

This allows rapid redesign without touching component styles.

---

# Editing Guide

# Updating Text

Most content edits happen in:

```html
index.html
```

Examples:
- About section
- Project descriptions
- Contact info
- Social links
- Resume link

---

# Updating Colors

Inside:

```css
:root
```

Primary variables:

```css
--color-bg
--color-bg-alt
--color-text
--color-text-muted
--color-primary
```

---

# Updating Fonts

Inside `<head>`:

```html
<link href="https://fonts.googleapis.com/..." />
```

Then update:

```css
--font-main
```

Current font:
- Inter

Recommended alternatives:
- Geist
- Satoshi
- General Sans
- IBM Plex Sans

---

# Updating Layout Width

Inside `:root`:

```css
--container-width
--container-narrow
```

---

# Responsive Behavior

Responsive rules live at the bottom of:

```css
style.css
```

Current mobile breakpoint:

```css
@media (max-width: 768px)
```

---

# Sections

The site uses reusable section structure:

```html
<section class="section">
```

Alternative background:

```html
<section class="section section-alt">
```

---

# Current Site Structure

```text
Header
Hero
About
Projects
Experience
Contact
Footer
```

---

# Adding New Sections

Duplicate this structure:

```html
<section class="section">
  <div class="container">

    <div class="section-header">
      <p class="section-label">Label</p>
      <h2>Section Title</h2>
    </div>

    CONTENT

  </div>
</section>
```

---

# Project Cards

Project cards use:

```html
<article class="card">
```

To add another project:
- duplicate an existing card
- replace content

Grid auto-adjusts responsively.

---

# Buttons

Primary button:

```html
<a class="btn btn-primary">
```

Secondary button:

```html
<a class="btn btn-secondary">
```

---

# Deployment

# Cloudflare Pages Setup

Recommended deployment architecture:

```text
GitHub
  ↓
Cloudflare Pages
  ↓
Custom Domain
```

---

# Deployment Steps

## 1. Push to GitHub

Repository structure should look like:

```text
index.html
style.css
README.md
```

---

## 2. Create Cloudflare Pages Project

Cloudflare Dashboard:

```text
Workers & Pages
→ Create Application
→ Pages
→ Connect to Git
```

---

## 3. Build Settings

Since this is static HTML:

```text
Framework preset: None
Build command: (leave blank)
Build output directory: /
```

---

## 4. Deploy

Cloudflare automatically:
- builds
- deploys
- provisions SSL
- distributes globally

---

# Updating the Site

Standard workflow:

```bash
git add .
git commit -m "Update site"
git push
```

Cloudflare auto-deploys.

No manual uploads required.

---

# Recommended Future Improvements

## Near-Term

- add real project pages
- replace placeholder links
- add resume PDF
- add favicon
- connect custom domain
- improve SEO metadata

---

## Medium-Term

Potential additions:
- blog
- writing section
- case studies
- analytics
- contact form
- dark/light theme toggle

---

## Long-Term

Possible migration paths:
- Astro
- Next.js
- Tailwind
- CMS integration

Current structure was designed to support migration later.

---

# Performance Philosophy

The site intentionally avoids:
- heavy JavaScript
- animation libraries
- frontend frameworks
- unnecessary dependencies

Goals:
- fast load times
- low maintenance
- resilience
- simplicity

---

# SEO Notes

Current SEO includes:
- title
- meta description
- semantic HTML

Recommended additions later:
- OpenGraph tags
- Twitter cards
- sitemap.xml
- robots.txt
- structured metadata

---

# Accessibility Notes

The site currently includes:
- semantic HTML
- readable contrast
- responsive scaling
- keyboard-safe navigation

Future improvements:
- ARIA labels
- skip navigation
- reduced motion support

---

# Recommended Content Strategy

Keep sections concise.

Strong portfolio sites usually emphasize:
- clarity
- specificity
- outcomes
- thoughtful writing

Avoid:
- excessive buzzwords
- large walls of text
- unnecessary animations

---

# Suggested Next Files

Potential future additions:

```text
about.html
projects.html
writing.html
contact.html
```

---

# Suggested Assets Folder

```text
images/
├── headshot.jpg
├── project-1.png
├── project-2.png
```

---

# Notes for Future AI Assistance

If using AI tools later:
- preserve semantic structure
- preserve CSS variables
- avoid unnecessary frameworks
- prefer maintainability over novelty
- keep site mostly static unless dynamic behavior is required

---

# Recommended Tech Philosophy Going Forward

Default toward:
- simplicity
- portability
- low dependency count
- readability
- performance

Avoid premature complexity.

This site should remain understandable by a single person without specialized tooling.

---
