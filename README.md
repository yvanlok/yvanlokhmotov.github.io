# Yvan Lokhmotov's Portfolio

A professional portfolio website showcasing ML projects, software development, and EPQ research.

**Live Site**: https://ylokhmotov.dev

## Running the Site Locally

1. Make sure you have Ruby and Bundler installed
2. Navigate to the project directory:
   ```powershell
   cd "E:\Projects\Web\Portfolio Website"
   ```
3. Install dependencies (first time only):
   ```powershell
   bundle install
   ```
4. Start the Jekyll server:
   ```powershell
   bundle exec jekyll serve
   ```
5. Open your browser to `http://127.0.0.1:4000/`

## Adding New Pages

### Adding a New Project

Simply create a new markdown file in the `projects/` directory (e.g., `projects/my-project.md`):

```markdown
---
layout: page
title: "My Project Title"
date: 2025-11-15
tags: [Python, Machine Learning, etc]
featured: true
summary: "A brief one-sentence description of your project"
---

# My Project Title

## Overview

Project description here...

## Tech Stack

- Python
- PyTorch
- etc.

[View on GitHub](https://github.com/yvanlok/my-project)
```

**That's it!** The project will automatically appear on the `/projects` page. Projects are sorted by date (newest first) and display:

- Title (from frontmatter)
- Summary (from frontmatter)
- Tags (from frontmatter)
- Automatic link to the full project page

No need to manually edit `projects/index.md` anymore!

### Adding a Journal Entry

Create a new markdown file in the `journal/` directory with the date format `YYYY-MM-DD-title.md`:

```markdown
---
layout: page
title: "Journal Entry Title"
date: 2025-11-15
---

# Journal Entry Title

Content of your journal entry...
```

## Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch. Check deployment status at:
https://github.com/yvanlok/yvanlokhmotov.github.io/actions
