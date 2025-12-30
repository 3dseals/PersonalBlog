# Tech Stack

## Framework
- Hexo 3.4.3 - Static site generator for blogs
- Node.js runtime

## Theme
- tranquilpeak - Feature-rich responsive theme with sidebar navigation

## Key Dependencies
- hexo-deployer-git - Git deployment
- hexo-generator-archive/category/tag/index - Content generators
- hexo-generator-feed - RSS/Atom feed generation
- hexo-generator-searchdb - Search functionality
- hexo-renderer-ejs - EJS template rendering
- hexo-renderer-marked - Markdown rendering
- hexo-renderer-stylus - Stylus CSS preprocessing
- hexo-server - Local development server

## Common Commands

```bash
# Start local dev server (preview at http://localhost:4000)
hexo s

# Create new post
hexo n "Post Title"

# Generate static files
hexo g

# Deploy to GitHub Pages
hexo d

# Clean cache and generated files
hexo clean

# Full rebuild and deploy
hexo clean && hexo g && hexo d

# Create new page
hexo n page "page-name"
```

## Deployment
- Target: GitHub Pages (git@github.com:ibunnyteam/ibunnyteam.github.io.git)
- Branch: master
- Uses SSH for deployment (requires SSH key setup)

## Configuration Files
- `_config.yml` - Main Hexo configuration
- `themes/tranquilpeak/_config.yml` - Theme configuration
