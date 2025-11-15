# GitHub Pages Configuration Guide

## Current Status

Your site is now configured to work with GitHub Pages using:

- ✅ `github-pages` gem for dependency compatibility
- ✅ GitHub Actions workflow for automated deployment
- ✅ Jekyll 3.10.0 (GitHub Pages compatible version)
- ✅ Additional plugins: jekyll-feed, jekyll-seo-tag, jekyll-sitemap

## Next Steps: Enable GitHub Actions Deployment

You need to configure your repository to use GitHub Actions for deployment:

### 1. Go to Repository Settings

Visit: https://github.com/yvanlok/yvanlokhmotov.github.io/settings/pages

### 2. Change Build and Deployment Source

- Under "Build and deployment"
- Change **Source** from "Deploy from a branch" to **"GitHub Actions"**

### 3. Wait for Deployment

- The GitHub Actions workflow will automatically trigger
- Check the Actions tab to see the deployment progress: https://github.com/yvanlok/yvanlokhmotov.github.io/actions
- First deployment usually takes 2-3 minutes

### 4. Verify Deployment

Once the action completes, your site will be live at:

- Primary URL: https://yvanlok.github.io/yvanlokhmotov.github.io/
- Custom domain (after DNS setup): https://ylokhmotov.dev

## What Changed

### Gemfile

- Replaced `gem "jekyll", "~> 4.4.1"` with `gem "github-pages", group: :jekyll_plugins`
- This ensures all dependencies match GitHub Pages exactly

### \_config.yml

- Added additional plugins: `jekyll-seo-tag`, `jekyll-sitemap`
- These are included in github-pages gem and enhance SEO

### GitHub Actions Workflow

- Created `.github/workflows/jekyll.yml`
- Automates building and deploying your Jekyll site
- Uses Ruby 3.2 and bundles gems automatically
- Deploys to GitHub Pages on every push to main branch

## Benefits of GitHub Actions Approach

1. **No Dependency Conflicts**: Uses exact same versions as GitHub Pages
2. **Faster Deployments**: Parallel processing and caching
3. **Better Error Messages**: See detailed build logs in Actions tab
4. **More Control**: Can customize build process if needed
5. **Modern Approach**: Recommended by GitHub for new sites

## Custom Domain Setup (ylokhmotov.dev)

Once GitHub Actions deployment is working:

1. Keep the CNAME file (already created)
2. Configure your DNS:
   - Add A records pointing to:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - OR add a CNAME record pointing to: `yvanlok.github.io`
3. In GitHub Pages settings, verify custom domain is set to `ylokhmotov.dev`
4. Enable "Enforce HTTPS" once DNS propagates (may take 24-48 hours)

## Local Development

To run the site locally (same environment as GitHub Pages):

```powershell
cd "E:\Projects\Web\Portfolio Website"
bundle install  # If you haven't already
bundle exec jekyll serve
```

Visit http://127.0.0.1:4000/

## Troubleshooting

### If build fails in GitHub Actions:

1. Check the Actions tab for error messages
2. Ensure all files are committed and pushed
3. Verify \_config.yml has valid YAML syntax

### If site doesn't update:

1. Clear your browser cache
2. Wait a few minutes for CDN to update
3. Check Actions tab to ensure deployment completed successfully

## Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Dependency Versions](https://pages.github.com/versions/)
