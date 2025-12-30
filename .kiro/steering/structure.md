# Project Structure

```
/
├── _config.yml              # Main Hexo configuration
├── package.json             # Node.js dependencies
├── source/                  # Content source files
│   ├── _posts/              # Blog posts (Markdown)
│   ├── all-archives/        # Archives page
│   ├── all-categories/      # Categories page
│   ├── all-tags/            # Tags page
│   └── resume/              # Resume/About page
├── scaffolds/               # Templates for new content
│   ├── post.md              # New post template
│   ├── page.md              # New page template
│   └── draft.md             # Draft template
└── themes/
    ├── landscape/           # Default Hexo theme (unused)
    └── tranquilpeak/        # Active theme
        ├── _config.yml      # Theme configuration
        ├── languages/       # i18n translations
        ├── layout/          # EJS templates
        ├── scripts/         # Theme helper scripts
        ├── source/          # Theme assets (CSS, JS, fonts, images)
        └── tasks/           # Grunt build tasks
```

## Content Conventions

### Post Naming
Posts follow the pattern: `YYYY-MM-DD-title.md`

### Post Front Matter
```yaml
title: Post Title
date: YYYY-MM-DD HH:mm:ss
tags: tag1 tag2 tag3
categories: category-name
```

### Language
- Primary content language: Chinese (zh-cn)
- Site timezone: Asia/Shanghai

### Assets
- Post assets: Enable `post_asset_folder: true` - create folder with same name as post
- Theme images: `themes/tranquilpeak/source/_images/` (dev) or `source/assets/images/` (prod)

### Permalinks
URL structure: `/:year/:month/:day/:title/`
