# statiq-theme-terminal-css

A [Statiq Web](https://statiq.dev/web) theme based on [CleanBlog](https://github.com/statiqdev/CleanBlog) and styled with [terminal-css](https://github.com/panr/terminal-css).

## Features

- Terminal-inspired dark theme (monospace fonts, accent colours)
- Blog posts with tags, archive listing, and pagination
- RSS and Atom feeds
- Optional search (via Statiq's built-in search index)
- Optional comments via [Giscus](https://giscus.app)
- Syntax highlighting powered by [PrismJS](https://prismjs.com)
- Override-friendly partial system (same extension points as CleanBlog)

## Usage

This repository is a [Statiq Web](https://statiq.dev/web) theme. To use it:

### As a theme (NuGet package approach)

Reference this theme from your Statiq Web project's `settings.yml`:

```yaml
Theme: statiq-theme-terminal-css
```

### As a direct copy

Copy the contents of the `input/` directory and `settings.yml` into your own Statiq Web project.

## Configuration

Add any of the following keys to your `settings.yml` to customise the theme:

| Key | Default | Description |
|-----|---------|-------------|
| `SiteTitle` | `My Blog` | Site name shown in the header |
| `SiteDescription` | *(none)* | Site description used in meta tags |
| `Copyright` | Current year | Footer copyright text |
| `PostSources` | `posts/**/*` | Glob pattern for post source files |
| `PageSources` | `pages/**/*` | Glob pattern for page source files |

### Giscus Comments

To enable comments, add the following to `settings.yml`:

```yaml
GiscusRepo: owner/repo
GiscusRepoId: R_...
GiscusCategory: Announcements
GiscusCategoryId: DIC_...
```

## File Structure

```
input/
├── css/
│   └── terminal.css          # terminal-css stylesheet
├── js/
│   └── terminal-blog.js      # Quicklink prefetching
├── posts/
│   └── index.cshtml          # Posts archive
├── tags/
│   └── index.cshtml          # Tags archive
├── _layout.cshtml            # Main HTML layout
├── _navigation.cshtml        # Site header / nav bar
├── _header.cshtml            # Page title / post header
├── _footer.cshtml            # Site footer
├── _navbar.cshtml            # Nav links (override to customise)
├── _post.cshtml              # Single post preview card
├── _posts.cshtml             # Post list with pagination
├── _copyright.cshtml         # Copyright line
├── _post-comments.cshtml     # Comment section (Giscus)
├── _head.cshtml              # Extra <head> content (empty stub)
├── _scripts.cshtml           # Extra scripts (empty stub)
├── _sidebar.cshtml           # Sidebar (empty stub)
├── _common-after-content.cshtml   # After any content (empty stub)
├── _post-after-content.cshtml     # After post content (empty stub)
├── _page-after-content.cshtml     # After page content (empty stub)
├── index.cshtml              # Home page (latest posts + tag cloud)
├── search.cshtml             # Search page
└── feed.yml                  # RSS / Atom feed
settings.yml                  # Default site settings
```

## Credits

- Layout based on [CleanBlog](https://github.com/statiqdev/CleanBlog) by [Statiq](https://statiq.dev) (MIT)
- CSS theme by [terminal-css](https://github.com/panr/terminal-css) by [panr](https://github.com/panr) (MIT)
