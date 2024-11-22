# BaseTheme

A minimal Jekyll remote theme designed as a clean starting point for your website.

## License

This theme is released under [CC0](LICENSE) ("No Rights Reserved"). You can copy, modify, distribute and use the theme without attribution or permission. For more details, see the [LICENSE](LICENSE) file.

## Author

Created by Christopher Allen ([GitHub @ChristopherA](https://github.com/ChristopherA) | ChristopherA@LifeWithAlacrity.com)

## Demo & Template

See it in action: [Live Demo](https://christophera.github.io/BaseTheme-DemoSite/)

Want to use this theme? You can:
1. View the demo site's source code: [BaseTheme-DemoSite](https://github.com/ChristopherA/BaseTheme-DemoSite)
2. Use BaseTheme-DemoSite as a template to start your own site

The demo shows how to create both static pages and blog posts using BaseTheme.

## Quick Start

If you prefer to start from scratch rather than using the template:

1. Create a new Jekyll site and add these to your `Gemfile`:
    ```ruby
    source "https://rubygems.org"
    gem "jekyll", "~> 4.0"
    gem "jekyll-remote-theme"
    ```

2. Configure your `_config.yml`:
    ```yaml
    # Theme Settings
    remote_theme: "ChristopherA/BaseTheme@main"
    plugins:
      - jekyll-remote-theme

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

3. Create your home page `index.md`:
    ```yaml
    ---
    layout: default
    title: Home
    ---

    Welcome to your new site!
    ```

4. Create a sample post in `_posts/YYYY-MM-DD-title.md`:
    ```yaml
    ---
    layout: post
    title: "Your First Post"
    date: YYYY-MM-DD
    description: "Optional SEO description"
    ---

    Your post content here.
    ```

5. Deploy to GitHub Pages:
    Follow GitHub's official guide to [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site). Make sure to:
    - Create a new repository
    - Push your files to the appropriate branch (usually `main` or `gh-pages`)
    - Enable GitHub Pages in your repository settings

6. Optional: Run Jekyll locally:
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
