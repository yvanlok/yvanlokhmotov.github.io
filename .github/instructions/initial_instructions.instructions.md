---
applyTo: "**"
---

Provide project context and coding guidelines that AI should follow when generating code, answering questions, or reviewing changes.

Portfolio Site Overview

Site name: ylokhmotov.dev
Owner: Yvan Lokhmotov

Purpose:
A professional portfolio showcasing Yvan Lokhmotov’s academic projects, software tools, machine learning work, and EPQ research. Designed for:

University applications

Work experience / internship applications

Professional networking (CV, LinkedIn, Unifrog)

Audience:

University admissions tutors

Internship or work experience supervisors

Recruiters and technical mentors

Key Features:

Home page: Hero section, featured projects, skills snapshot, journal preview, links to CV, GitHub, LinkedIn

About page: Personal bio, education, skills, contact links

Projects page: Index of projects with tags and filters

Project detail pages: Individual pages for each project (EPQ, ffbeast, future projects), including overview, technical details, results, GitHub links

Journal: Chronological project writeups and reflections, easy to add future entries

CV page: Downloadable PDF, brief HTML preview

Contact page: LinkedIn, GitHub, email contact

Future extensibility: Ability to embed interactive demos or visualizations

Design:

Professional, minimal, clean layout

Mobile-first and responsive

Easy to maintain and extend

Step-by-Step Instructions for GitHub Copilot Agent

1. Create Repository
   gh repo create yvanlokhmotov.github.io \
    --public \
    --description "Yvan Lokhmotov portfolio website for projects, EPQ, and work experience" \
    --homepage "https://ylokhmotov.dev"
   git clone https://github.com/yvanlokhmotov/yvanlokhmotov.github.io.git
   cd yvanlokhmotov.github.io

2. Initialize Jekyll Site
   jekyll new . --force
   rm -rf \_posts
   rm -rf about.md index.markdown

3. Configure \_config.yml
   title: "Yvan Lokhmotov Portfolio"
   email: "your-email@example.com"
   description: "Portfolio of Yvan Lokhmotov – ML projects, software, and EPQ."
   baseurl: "" # leave empty for GitHub Pages
   url: "https://ylokhmotov.dev"
   github_username: "yvanlokhmotov"
   theme: minima
   plugins:

- jekyll-feed

4. Add Custom Domain
   echo "ylokhmotov.dev" > CNAME

5. Create Directory Structure
   mkdir -p projects journal assets/images assets/pdf \_layouts \_includes

6. Add Placeholder Pages
   Home (index.md)

---

layout: default
title: Home

---

# Yvan Lokhmotov Portfolio

I build ML and software projects. Open source code on [GitHub](https://github.com/yvanlokhmotov).

[View Projects](/projects/) | [Download CV](/assets/pdf/CV_Yvan_Lokhmotov.pdf)

## About (about.md)

layout: default
title: About

---

## About Me

I am an A-level student building ML and software projects for F1 and research. Skilled in Python, PyTorch, TabNet, pandas, and Git.

### Education

- Current School: [Your School]
- Subjects: Maths, Further Maths, Physics, Chemistry, Computer Science

### Contact

- [GitHub](https://github.com/yvanlokhmotov)
- [LinkedIn](https://linkedin.com/in/yvanlokhmotov)

## Projects Index (projects/index.md)

layout: default
title: Projects

---

# Projects

- [EPQ Project](/projects/epq.md)
- [ffbeast Project](/projects/ffbeast.md)

7. Add Starter Project Pages
   EPQ (projects/epq.md)

---

title: "EPQ — F1 Predictive Model"
date: 2025-11-15
tags: [machine learning, EPQ, motorsport]
repo: "https://github.com/yvanlokhmotov/EPQ"
featured: true
summary: "Neural nets and TabNet for race prediction with backtesting to prevent leakage."

---

# Overview

Predictive modelling for Formula 1 race finishing positions.

# Role

- Dataset collection and cleaning
- Model design using PyTorch and TabNet
- Evaluation and backtesting

# Tech stack

Python, PyTorch, TabNet, pandas

# Results

Metrics and plots displayed here (placeholder)

## ffbeast (projects/ffbeast.md)

title: "ffbeast Project"
date: 2025-11-15
tags: [software, ML, motorsport]
repo: "https://github.com/yvanlokhmotov/ffbeast"
featured: true
summary: "Tool for Formula 1 telemetry analysis and predictive simulations."

---

# Overview

Software tool for F1 telemetry analysis and predictive simulations.

# Role

- Designed software architecture
- Integrated ML models and telemetry parsing
- Created plots and dashboards

# Tech stack

Python, pandas, FastF1, PyTorch

8. Add Placeholder CV
   touch assets/pdf/CV_Yvan_Lokhmotov.pdf

9. Add Journal Template
   Example journal post

journal/2025-11-15-first-entry.md

---

title: "First Journal Entry"
date: 2025-11-15
tags: [EPQ]

---

Started documenting projects. Added EPQ and ffbeast projects to portfolio.

10. Commit and Push
    git add .
    git commit -m "Initial portfolio structure with EPQ and ffbeast placeholders"
    git push origin main

11. Set Up GitHub Pages

Settings → Pages → Branch: main, folder: /

Custom domain: ylokhmotov.dev

Enable HTTPS

12. Future Automation Notes

Add new projects by creating markdown in /projects with frontmatter

Add new journal posts by creating markdown in /journal

Optional GitHub Actions workflow to regenerate Jekyll site on push
