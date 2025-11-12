# Visu Vista

Welcome to the Visu Vista company website repository. This is a static website built with [Hugo](https://gohugo.io/) and styled with the [Hugoplate](https://themes.gohugo.io/themes/hugoplate/) theme.

## About

Visu Vista - Your Vision, Our Mission

## Prerequisites

Before you begin, ensure you have the following installed:
- [Hugo Extended](https://gohugo.io/installation/) v0.144.0 or later
- [Git](https://git-scm.com/downloads)
- [Go](https://golang.org/dl/) 1.21 or later (for Hugo modules)

## Getting Started

1. Clone this repository:
```bash
git clone https://github.com/ArdonToonstra/visuvista.git
cd visuvista
```

2. Initialize and update the theme submodule and Hugo modules:
```bash
git submodule update --init --recursive
hugo mod get -u
```

3. Build the site:
```bash
hugo
```

Or start the development server:
```bash
hugo server
```

The site will be available at `http://localhost:1313/`

## Project Structure

```
.
├── archetypes/       # Content templates
├── assets/           # CSS, JS, and other assets  
│   ├── css/          # Stylesheets
│   └── images/       # Images and graphics
├── content/          # Site content (pages, blog posts, etc.)
│   └── english/      # English language content
├── data/             # Data files (JSON, YAML, TOML)
├── i18n/             # Internationalization files
├── layouts/          # Custom layout templates
├── static/           # Static files served as-is
├── themes/           # Hugo themes
│   └── hugoplate/    # Hugoplate theme (git submodule)
├── config/           # Site configuration
│   └── _default/     # Default configuration
├── hugo.toml         # Main Hugo configuration
├── go.mod            # Go module dependencies
├── .gitignore        # Git ignore rules
└── README.md         # This file
```

## Configuration

The site is configured using multiple files:

- **Main configuration**: `hugo.toml` - Site title, baseURL, theme settings
- **Theme parameters**: `config/_default/params.toml` - Colors, fonts, logos, features
- **Menu configuration**: `config/_default/menus.en.toml` - Navigation menus
- **Language settings**: `config/_default/languages.toml` - Language-specific settings
- **Module configuration**: `config/_default/module.toml` - Hugo module dependencies

### Key Settings to Customize

Edit `hugo.toml`:
- `baseURL`: Your website domain
- `title`: Website title

Edit `config/_default/params.toml`:
- `logo_text`: Company name shown when logo is missing
- `copyright`: Footer copyright text
- `metadata`: SEO metadata (keywords, description, author)

## Adding Content

To create a new blog post:
```bash
hugo new content/english/blog/my-new-post.md
```

To create a new page:
```bash
hugo new content/english/pages/my-new-page.md
```

## Building for Production

To build the site for production:

```bash
hugo --minify
```

The generated site will be in the `public/` directory.

## Theme

This site uses the [Hugoplate](https://github.com/zeon-studio/hugoplate) theme, which includes:
- Tailwind CSS for styling
- Responsive design
- Dark mode support
- SEO optimized
- Multiple page layouts
- Blog functionality
- Contact forms
- And much more!

The theme is added as a git submodule and uses Hugo modules for additional functionality.

## Troubleshooting

### Hugo Module Issues

If you encounter module-related errors:
```bash
hugo mod clean
hugo mod get -u
```

### Theme Not Loading

Ensure the theme submodule is initialized:
```bash
git submodule update --init --recursive
```

### Build Errors

Make sure you're using Hugo Extended version 0.144.0 or later:
```bash
hugo version
```

## License

This project is licensed under the MIT License - see the theme's license for details.

## Support

For issues related to:
- This website: Open an issue in this repository
- Hugo: Visit [Hugo Documentation](https://gohugo.io/documentation/)
- Hugoplate theme: Visit [Hugoplate Repository](https://github.com/zeon-studio/hugoplate)
