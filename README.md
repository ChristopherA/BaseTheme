# BaseTheme

A Jekyll remote theme, crafted as a lean foundation for static sites on GitHub Pages.

For examples of building on this foundation, see the [demo site](https://christophera.github.io/BaseTheme-DemoSite/) and its [source](https://github.com/ChristopherA/BaseTheme-DemoSite).

## Features

- 🪶 Minimal, no-bloat foundation
- 📝 Automatic front matter generation
  - Page titles from first heading
  - Layouts based on content location
- 🔍 SEO-friendly metadata
- 🗺️ Search engine sitemap
- 📱 Mobile-first responsive design
- ♿️ WCAG accessibility compliant
- 🌙 Dark mode support
- 🖨️ Print-friendly styles
- 🚫 No JavaScript required
- 🎨 Easy to customize

## Demo & Template

See it in action:
- [Live Demo](https://christophera.github.io/BaseTheme-DemoSite/) - shows both basic usage and optional features
- [Demo Source](https://github.com/ChristopherA/BaseTheme-DemoSite) - includes additional blog features

## Quick Start

If you prefer to start from scratch rather than using the template:

1. Configure your `_config.yml`:
    ```yaml
    # Theme Settings
    remote_theme: "ChristopherA/BaseTheme@main"

    # Required Plugins
    plugins:
      - jekyll-remote-theme         # Required for remote themes
      - jekyll-seo-tag             # Required for SEO meta tags
      - jekyll-sitemap             # Required for search engines
      - jekyll-titles-from-headings # Required for automatic page titles
      - jekyll-default-layout      # Required for automatic layouts

    # Site Settings
    title: "Your Site Title"
    description: "Your site description"
    url: "https://yourusername.github.io"  # Root URL where site will be hosted
    baseurl: "/your-repo-name"  # Leave empty if hosting at root URL

    # Optional Settings
    navigation:
      - title: Home
        url: /
      - title: About
        url: /about/
    date_format: "%B %d, %Y"  # Default date format for posts

    # Jekyll Settings
    markdown: kramdown
    collections:
      pages:
        output: true
    ```

2. Create your home page `index.md`:
    ```yaml
    ---
    description: "Optional SEO description"  # Only if needed
    ---

    # Welcome to Your Site

    Your content starts here!
    ```

3. Create a sample post in `_posts/YYYY-MM-DD-title.md` (optional - only if you want blog features):
    ```yaml
    ---
    date: YYYY-MM-DD              # Required for posts
    description: "Optional SEO description"
    ---

    # Your First Post

    Your post content here.
    ```

4. Deploy to GitHub Pages:
    Follow GitHub's official guide to [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site). Make sure to:
    - Create a new repository
    - Push your files to the appropriate branch (usually `main` or `gh-pages`)
    - Enable GitHub Pages in your repository settings

5. Optional: Run Jekyll locally:
   SIDENOTE: Personally, I rarely do this, and instead rely on the free GitHub Pages infrastructure.

   To run Jekyll locally, you'll need install Ruby and Jekyll for your operating system:
   - macOS: `brew install ruby jekyll`
   - Ubuntu/Debian: `sudo apt install ruby-full jekyll`
   - Windows: See [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/)

   Then run:
    ```zsh
    bundle install   # Install required gems
    jekyll serve     # Start local server at http://localhost:4000
    ```
   More details for running Jekyll locally are at the official [Jekyll Installation Guide](https://jekyllrb.com/docs/installation/).

## Layouts

BaseTheme uses automatic layout detection based on content location:

1. Posts in `_posts/` → `post` layout
2. Files named `index.md` → `home` layout
3. Other `.md` files → `page` layout
4. `.html` files → `default` layout

You can override any automatic layout by specifying it in front matter:
```yaml
---
layout: custom-layout
---
```

## Front Matter

Required only for posts:
```yaml
---
date: YYYY-MM-DD   # Date required for blog posts
---
```

Optional front matter:
```yaml
---
description: "SEO description"  # Optional: recommended for SEO
permalink: /custom-url/         # Optional: custom URL path
title: "Override Title"         # Optional: only if different from first heading
layout: "custom"               # Optional: override automatic layout
---
```

## License

This theme is released under [CC0](LICENSE) ("No Rights Reserved"). You can copy, modify, distribute and use the theme without attribution or permission. For more details, see the [LICENSE](LICENSE) file.

## Author

Created by Christopher Allen ([GitHub @ChristopherA](https://github.com/ChristopherA) | ChristopherA@LifeWithAlacrity.com)
