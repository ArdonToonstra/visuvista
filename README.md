# Visu Vista

Welcome to the Visu Vista company website repository. This is a static website built with [Hugo](https://gohugo.io/) and styled with the [Hugoplate](https://themes.gohugo.io/themes/hugoplate/) theme.

## About

Visu Vista - Your Vision, Our Mission

## Prerequisites

Before you begin, ensure you have the following installed:
- [Hugo Extended](https://gohugo.io/installation/) (v0.121.0 or later)
- [Git](https://git-scm.com/downloads)

## Getting Started

1. Clone this repository:
```bash
git clone https://github.com/ArdonToonstra/visuvista.git
cd visuvista
```

2. Initialize and update the theme submodule:
```bash
git submodule update --init --recursive
```

3. Start the development server:
```bash
hugo server
```

The site will be available at `http://localhost:1313/`

## Project Structure

```
.
├── archetypes/       # Content templates
├── assets/           # CSS, JS, and other assets
├── content/          # Site content (pages, blog posts, etc.)
├── data/             # Data files
├── i18n/             # Internationalization files
├── layouts/          # Custom layout templates
├── static/           # Static files (images, etc.)
├── themes/           # Hugo themes
│   └── hugoplate/    # Hugoplate theme (git submodule)
├── config/           # Site configuration
├── hugo.toml         # Main Hugo configuration
└── README.md         # This file
```

## Building for Production

To build the site for production:

```bash
hugo --minify
```

The generated site will be in the `public/` directory.

## Configuration

- Main configuration: `hugo.toml`
- Theme parameters: `config/_default/params.toml`
- Menu configuration: `config/_default/menus.en.toml`
- Language settings: `config/_default/languages.toml`

## Adding Content

To create a new blog post:

```bash
hugo new content/blog/my-new-post.md
```

To create a new page:

```bash
hugo new content/pages/my-new-page.md
```

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

## License

This project is licensed under the MIT License - see the theme's license for details.

## Support

For issues related to:
- This website: Open an issue in this repository
- Hugo: Visit [Hugo Documentation](https://gohugo.io/documentation/)
- Hugoplate theme: Visit [Hugoplate Repository](https://github.com/zeon-studio/hugoplate)
