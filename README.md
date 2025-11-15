# Yvan Lokhmotov Portfolio Website

Professional portfolio showcasing academic projects, software tools, machine learning work, and EPQ research.

## Site Information

- **Site URL**: https://ylokhmotov.dev
- **GitHub Repository**: https://github.com/yvanlok/yvanlokhmotov.github.io
- **Owner**: Yvan Lokhmotov

## Purpose

This portfolio is designed for:
- University applications
- Work experience / internship applications
- Professional networking (CV, LinkedIn, Unifrog)

## Current Features

- Home page with hero section and featured projects
- About page with personal bio, education, and skills
- Projects page with EPQ and ffbeast projects
- Journal for project writeups and reflections
- Placeholder for downloadable CV

## Tech Stack

- **Framework**: Jekyll (static site generator)
- **Theme**: Minima
- **Hosting**: GitHub Pages
- **Custom Domain**: ylokhmotov.dev

## Local Development

To run the site locally:

```powershell
cd "E:\Projects\Web\Portfolio Website"
bundle exec jekyll serve
```

The site will be available at `http://127.0.0.1:4000/`

## File Structure

```
.
├── _config.yml           # Jekyll configuration
├── index.md              # Home page
├── about.md              # About page
├── projects/
│   ├── index.md          # Projects listing
│   ├── epq.md            # EPQ project detail
│   └── ffbeast.md        # ffbeast project detail
├── journal/
│   └── 2025-11-15-first-entry.md
├── assets/
│   ├── images/           # Image assets
│   └── pdf/
│       └── CV_Yvan_Lokhmotov.pdf  # CV (placeholder)
├── _layouts/             # Custom layouts (if needed)
└── _includes/            # Reusable components (if needed)
```

## Adding New Content

### Adding a New Project

Create a new markdown file in the `projects/` directory:

```markdown
---
layout: default
title: "Project Title"
date: YYYY-MM-DD
tags: [tag1, tag2]
repo: "https://github.com/yvanlokhmotov/project-name"
featured: true
summary: "Brief project description"
---

# Project Title

## Overview
...

## Role
...

## Tech stack
...

[View on GitHub]({{ page.repo }})
```

Then add a link to it in `projects/index.md`.

### Adding a Journal Entry

Create a new markdown file in the `journal/` directory with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: default
title: "Journal Entry Title"
date: YYYY-MM-DD
tags: [tag1, tag2]
---

# Journal Entry Title

Content here...
```

## Next Steps

1. **Add CV**: Replace the placeholder `assets/pdf/CV_Yvan_Lokhmotov.pdf` with your actual CV
2. **Configure Custom Domain**: 
   - Go to GitHub repository settings → Pages
   - Verify that "ylokhmotov.dev" is set as the custom domain
   - Enable "Enforce HTTPS"
   - Configure DNS settings for your domain to point to GitHub Pages:
     - Add an A record pointing to GitHub's IPs: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
     - Or add a CNAME record pointing to: yvanlok.github.io
3. **Add More Projects**: Create additional project pages as you complete new work
4. **Add Images**: Place project screenshots and diagrams in `assets/images/`
5. **Customize Theme**: Modify `_layouts/` and `_includes/` for custom styling
6. **Add Interactive Demos**: Consider embedding interactive visualizations or demos in project pages

## GitHub Pages Setup

The site is configured to deploy from the `main` branch. Any push to `main` will trigger a rebuild and deploy.

## Contact

- **GitHub**: [yvanlokhmotov](https://github.com/yvanlokhmotov)
- **LinkedIn**: [yvanlokhmotov](https://linkedin.com/in/yvanlokhmotov)
- **Email**: yvanlokh@gmail.com
