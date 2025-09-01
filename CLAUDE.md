# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based static website for DZLabs GmbH using the Beautiful Jekyll theme. The site is hosted on GitHub Pages at dzlabsch.github.io and serves as a company website showcasing services and expertise.

## Build and Development Commands

### Core Jekyll Commands
- `bundle install`: Install Ruby gem dependencies
- `bundle exec jekyll serve`: Run local development server (usually at http://localhost:4000)
- `bundle exec jekyll serve --drafts`: Include draft posts in local development
- `bundle exec jekyll build`: Build the site for production (outputs to `_site/`)
- `bundle exec jekyll serve --livereload`: Run with automatic browser refresh
- `bundle update`: Update gem dependencies

### GitHub Pages Deployment
- Deployment is automatic via GitHub Pages when pushing to the `master` branch
- No manual build/deploy commands needed for production

## Site Architecture

### Jekyll Structure
- `_config.yml`: Main site configuration including theme settings, navigation, social links, and Jekyll options
- `_layouts/`: HTML templates for different page types (base, default, home, page, post, minimal)
- `_includes/`: Reusable HTML components (header, footer, navigation, social media, analytics)
- `_data/`: YAML data files (currently contains UI text configurations)
- `_posts/`: Blog posts directory (currently empty - add markdown files here for blog content)
- `assets/`: Static assets including CSS, JavaScript, and images
- `_content/`: Additional content files

### Key Layout Types
- `layout: home`: Homepage with blog post listing (used in index.html)
- `layout: page`: Standard pages (used for About page and general content)
- `layout: post`: Blog posts with navigation, tags, and social sharing
- `layout: minimal`: Clean layout without navigation/footer
- `layout: base`: Core template that other layouts inherit from

### Content Structure
- Pages created as `.md` or `.html` files in root directory
- Blog posts go in `_posts/` with naming convention: `YYYY-MM-DD-post-title.md`
- All content files require YAML front matter with layout specification

## Theme Customization

### Configuration
- Site metadata, navigation, and theme settings in `_config.yml`
- Color scheme and styling options configured in `_config.yml` (navbar-col, page-col, etc.)
- Social media links and contact information in `_config.yml`

### Assets
- Custom CSS can be added to `assets/css/`
- Images stored in `assets/img/`
- JavaScript files in `assets/js/`
- Site logo/avatar configured as `title-img` in `_config.yml`

### Content Pages
- About page: `aboutme.md` - company information and expertise
- Additional content in `_content/about.md`
- Homepage content controlled via `index.html` front matter

## Company Context

DZLabs GmbH is a Swiss IT consulting company specializing in:
- Open source monitoring/observability tools (Grafana, Prometheus, InfluxDB, ElasticSearch)
- Development stack: PowerShell, Python, Bash, .NET (C#), Node.js
- VMware virtualization and cloud solutions
- Founded by Dennis Zimmer (16x VMware vExpert)

## Common Development Tasks

### Adding Blog Posts
1. Create new file in `_posts/` with format: `YYYY-MM-DD-title.md`
2. Include YAML front matter with layout, title, subtitle, and tags
3. Write content in Markdown below the front matter

### Updating Site Configuration
- Modify `_config.yml` for site-wide changes
- Update navigation links in `navbar-links` section
- Modify social media links in `social-network-links` section

### Content Management
- Page content uses Markdown with YAML front matter
- Images referenced relative to site root: `/assets/img/filename.jpg`
- Internal links use Jekyll's `{{ site.baseurl }}` or relative paths

## Theme Features

### Built-in Components
- Responsive navigation with mobile menu
- Social media sharing buttons (configurable per post)
- Comments support (Disqus, Facebook, Utterances, Staticman)
- Google Analytics integration
- Tag system for blog posts
- SEO optimization with customizable meta tags
- RSS feed generation

### Supported Page Parameters
- `title`, `subtitle`: Page/post titles and descriptions
- `cover-img`: Hero images for posts
- `tags`: Post categorization
- `comments`: Enable/disable comments per page
- `social-share`: Control social sharing buttons
- `full-width`: Allow content to span full window width

## Important Notes

- This site uses Jekyll ~3.8 with kramdown markdown processor
- Beautiful Jekyll theme version 5.0.0
- No package.json - pure Jekyll/Ruby ecosystem
- Automatic GitHub Pages deployment from master branch
- Site configuration optimized for company/business use case
- Currently no blog posts - empty `_posts/` directory ready for content