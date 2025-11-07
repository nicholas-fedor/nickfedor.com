# Nick Fedor's Personal Website

## Description

This is a personal website for Nick Fedor, built using Hugo and the PaperMod theme.
It features a minimalist, SEO-friendly design optimized for performance and readability.
The website includes sections for a blog, projects, websites, and an about page.

## Features

- **Responsive Design**: Clean, mobile-friendly layout that adapts to different screen sizes.
- **Search Functionality**: Built-in search using Fuse.js for quick content discovery.
- **Social Sharing**: Easy sharing of posts on social media platforms.
- **Theme Support**: Default dark mode with a toggle option (currently disabled).
- **Content Features**:
  - Table of contents for blog posts.
  - Reading time estimates.
  - Code copy buttons for code blocks.
  - Syntax highlighting.
  - Breadcrumbs and post navigation.
  - Related posts suggestions.
  - Word count display.
- **Custom Styling**: Space-themed background image with semi-transparent overlays and blur effects for a cohesive dark aesthetic.
- **Performance Optimized**: Assets are fingerprinted, bundled, and minified using Hugo's pipeline.
- **SEO Friendly**: Includes meta tags, sitemaps, and RSS feeds.

## Technologies Used

- **Hugo**: Static site generator (minimum version 0.146.0 required by the theme).
- **PaperMod Theme**: A fast, clean, and responsive Hugo theme based on hugo-paper, providing built-in features like search, social sharing, and internationalization.
- **Markdown**: Content is written in Markdown with front matter for metadata.
- **CSS**: Custom styles processed via Hugo's asset pipeline.
- **HTML/JS**: Provided by the theme for interactivity and layout.
- **No External Dependencies**: The site is self-contained beyond Hugo itself.

## Installation and Setup

### Prerequisites

- Hugo installed on your system (version 0.146.0 or later). Download from [Hugo's official website](https://gohugo.io/getting-started/installing/).

### Steps

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/nicholas-fedor/nickfedor.com.git
   cd nickfedor.com
   ```

2. **Install Dependencies**:
   No additional dependencies are required beyond Hugo.

3. **Run Locally for Development**:

   ```bash
   hugo server
   ```

   This starts a local development server at `http://localhost:1313/`. Changes to content or configuration will be reflected automatically.

4. **Build the Site**:

   ```bash
   hugo
   ```

   This generates the static site in the `public/` directory.

5. **Deploy**:
   Upload the contents of the `public/` directory to your web hosting provider (e.g., Netlify, Vercel, or a traditional web server).

## Usage

### Adding Content

- Content is stored in the `content/` directory as Markdown files.
- Each page/post uses front matter for metadata (e.g., title, description, date).
- Example front matter:

  ```yaml
  ---
  title: "My Blog Post"
  description: "A description of the post"
  date: 2024-10-01
  ---
  ```

- Write content in Markdown below the front matter.

### Configuration

- Edit `config.toml` to update site settings, menus, social links, and parameters.
- Key configurations include base URL, language, theme settings, and enabled features.

### Customization

- Modify styles in `assets/css/custom.css` to change the appearance.
- Override theme templates by placing custom layouts in the `layouts/` directory.

### Building and Serving

- Use `hugo server` for development.
- Use `hugo` to build for production.
- The generated site in `public/` can be served by any static web server.

## Project Structure Overview

```text
nickfedor.com/
├── config.toml                 # Main configuration file (site metadata, parameters, menus)
├── content/                    # Markdown-based content
│   ├── _index.md              # Home page
│   ├── about/
│   │   └── index.md           # About page
│   ├── blog/
│   │   ├── _index.md          # Blog index
│   │   └── posts/             # Individual blog posts
│   ├── projects/
│   │   └── _index.md          # Projects section
│   └── websites/
│       └── _index.md          # Websites section
├── layouts/                    # Custom Hugo templates overriding theme defaults
│   ├── _default/
│   │   └── list.html          # Custom list template for sections/pages
│   └── partials/
│       ├── extend_head.html   # Injects custom CSS into page head
│       └── social_icons.html  # Renders social links
├── assets/                     # Custom assets processed by Hugo
│   └── css/
│       └── custom.css         # Custom styles (space-themed background, overlays)
├── static/                     # Static assets served directly
│   └── images/                # Images and media files
├── themes/
│   └── papermod/              # PaperMod theme codebase
└── public/                    # Generated static site output (not in source control)
```

- **`config.toml`**: Central configuration defining site title, base URL, language, menus, social links, and theme parameters.
- **`content/`**: Organized into sections with index pages and individual posts.
- **`layouts/`**: Custom overrides for theme templates, including list views and partials.
- **`assets/`**: Custom CSS processed and minified by Hugo.
- **`static/`**: Unprocessed static files like images.
- **`themes/papermod/`**: Full theme source, including layouts, CSS, JS, and i18n files.
- **`public/`**: Output directory for the built site (excluded from version control).

## Customization Details

### Site Configuration

Edit `config.toml` to customize:

- **Site Metadata**: Title, description, base URL, language.
- **Menus**: Navigation items (Home, Blog, Projects, Websites, About) with weights for ordering.
- **Social Links**: Icons and URLs for Twitter, Reddit, GitHub, LinkedIn.
- **Parameters**: Enable/disable features like reading time, table of contents, search, social sharing, breadcrumbs, etc.
- **Theme Settings**: Default color scheme (dark mode), theme toggle availability.

Example menu configuration:

```toml
[[menu.main]]
  identifier = "home"
  name = "Home"
  url = "/"
  weight = 10
```

### Styling

- Custom styles are in `assets/css/custom.css`.
- Current customizations include:
  - Space-themed background image `background.png` (full-size: `eso0932a-6000x2523.png`) applied site-wide with cover sizing.
  - Fixed header height (90px).
  - Semi-transparent backgrounds (`rgba(0,0,0,0.4)`) with blur effects for content areas.
  - Overrides for padding, borders, and positioning to maintain a dark aesthetic.

To modify, edit the CSS file and rebuild the site.

### Layout Overrides

- Custom templates in `layouts/` override theme defaults.
- `layouts/_default/list.html`: Handles section listings, including recent posts on the home page, pagination, and post entries with covers and metadata.
- `layouts/partials/extend_head.html`: Injects minified custom CSS.
- `layouts/partials/social_icons.html`: Renders social links from config.

### Content Management

- Add new posts in `content/blog/posts/` as Markdown files with front matter.
- Use taxonomies (categories/tags) for organization (generated automatically).
- Include cover images in post front matter for visual appeal.

### Theme Features

- Leverages PaperMod's multilingual support (i18n files available).
- SEO optimizations, responsive images, and archives.
- Shortcodes for advanced content (e.g., figures, collapsible sections).

## Deployment

- Build the site with `hugo` and deploy the `public/` directory.
- Suitable for static hosting services like GitHub Pages, Netlify, or Vercel.
- For self-hosting, serve the `public/` directory with a web server like Nginx or Apache.

## Contributing

This is a personal website, but contributions for improvements (e.g., bug fixes, feature suggestions) are welcome via pull requests or issues on the repository.

## License

This project uses the PaperMod theme, which is licensed under the MIT License. See `themes/papermod/LICENSE` for details.

## Acknowledgments

- Built with [Hugo](https://gohugo.io/) and the [PaperMod theme](https://github.com/adityatelange/hugo-PaperMod).
- Space background image courtesy of ESO.

For more information, visit [nickfedor.com](https://nickfedor.com/).
