# Visu Vista - Hugo Multilingual Website

## GitHub Pages Deployment Setup

This repository includes an automated GitHub Actions workflow that deploys the Hugo site to GitHub Pages when you push to the `main` or `develop` branches.

### Setup Instructions

#### 1. Enable GitHub Pages
1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **GitHub Actions**

#### 2. Repository Permissions
The workflow is already configured with the necessary permissions:
- `contents: read` - To checkout the repository
- `pages: write` - To deploy to GitHub Pages
- `id-token: write` - For secure deployment

#### 3. Branch Configuration
The workflow triggers on:
- **Push to `main` branch** - Production deployment
- **Push to `develop` branch** - Development/staging deployment
- **Manual trigger** - Can be run manually from the Actions tab

### Workflow Features

#### 🚀 **Automated Deployment**
- Builds Hugo site with production optimizations
- Deploys to GitHub Pages automatically
- Supports multilingual content (EN, ES, NL)

#### 🔧 **Build Process**
- **Hugo Version**: 0.150.0 (extended)
- **Node.js**: Version 20 with npm caching
- **Sass Compilation**: Dart Sass for styling
- **Minification**: CSS and JS minification enabled
- **Asset Processing**: Optimized images and resources

#### 📦 **Dependencies**
- Automatically installs npm dependencies if `package.json` exists
- Supports both `npm install` and `npm ci` based on lockfile presence
- Includes Hugo modules and theme dependencies

#### 🌐 **Site Configuration**
- **Base URL**: Automatically configured for GitHub Pages
- **Environment**: Production mode for optimized builds
- **Multilingual**: Full support for EN/ES/NL languages
- **Theme**: Hugoplate theme with custom overrides

### Deployment Process

1. **Trigger**: Push to `main` or `develop` branch
2. **Build**: 
   - Checkout code with submodules
   - Setup Hugo and Node.js
   - Install dependencies
   - Build site with optimizations
3. **Deploy**: Upload and deploy to GitHub Pages
4. **Notify**: Display deployment status and site URL

### Branch Strategy

- **`main` branch**: Production deployments → `https://ardontoonstra.github.io/visuvista/`
- **`develop` branch**: Staging deployments → Same URL (overwrites)

> **Note**: Both branches deploy to the same GitHub Pages URL. Consider using different repositories or subfolders if you need separate staging/production URLs.

### Manual Deployment

You can also trigger deployments manually:
1. Go to **Actions** tab in your repository
2. Select **Deploy Hugo site to GitHub Pages**
3. Click **Run workflow**
4. Choose the branch to deploy from

### Troubleshooting

#### Common Issues:

1. **Build Failures**
   - Check Hugo version compatibility
   - Verify all content files have proper front matter
   - Ensure no broken internal links

2. **Deployment Failures**
   - Verify GitHub Pages is enabled in repository settings
   - Check repository permissions
   - Ensure the `public` folder is generated correctly

3. **Content Issues**
   - Verify all markdown files have `draft: false`
   - Check multilingual configuration in `hugo.toml`
   - Ensure all required translation files exist

#### Logs and Debugging:

- Check the **Actions** tab for detailed build logs
- Look for error messages in the build or deploy steps
- Verify the generated site in the artifact uploads

### Site Structure

```
visuvista/
├── .github/workflows/hugo-deploy.yml    # Deployment workflow
├── content/                             # Multilingual content
│   ├── en/                             # English content
│   ├── es/                             # Spanish content
│   └── nl/                             # Dutch content
├── layouts/                            # Custom templates
├── static/                             # Static assets
├── assets/                             # Processed assets
├── config/                             # Hugo configuration
└── themes/hugoplate/                   # Theme files
```

### Next Steps

1. **Push your changes** to `main` or `develop` branch
2. **Monitor the deployment** in the Actions tab
3. **Visit your site** at the GitHub Pages URL
4. **Update content** and push again to redeploy

---

**Site URL**: Will be available at `https://ardontoonstra.github.io/visuvista/` once deployed.

**Deployment Status**: Check the Actions tab for real-time deployment status and logs.