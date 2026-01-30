# Documentation Template Setup Guide

This guide explains the documentation template structure created for TradieScribe.

## 📁 Repository Structure

```
docs-public/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── documentation-issue.md    # Template for reporting docs issues
│   │   └── feature-request.md        # Template for requesting new docs
│   ├── PULL_REQUEST_TEMPLATE.md      # Template for doc contributions
│   └── workflows/
│       ├── ci.yml                    # CI workflow for PRs
│       └── deploy-docs.yml           # Auto-deploy to GitHub Pages
├── docs/
│   ├── index.md                      # Documentation homepage
│   ├── getting-started.md            # Quick start guide
│   ├── faq.md                        # Frequently asked questions
│   ├── api/
│   │   └── index.md                  # API documentation
│   ├── guides/
│   │   ├── index.md                  # User guides index
│   │   └── best-practices.md         # Best practices guide
│   └── reference/                    # Technical reference (empty, ready for content)
├── .gitignore                        # Git ignore rules
├── CONTRIBUTING.md                   # Contribution guidelines
├── LICENSE                           # MIT License
├── README.md                         # Repository README
├── mkdocs.yml                        # MkDocs configuration
├── package.json                      # NPM scripts
└── requirements.txt                  # Python dependencies
```

## 🚀 Getting Started

### Local Development

1. **Install Python dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Serve documentation locally:**
   ```bash
   mkdocs serve
   ```
   Visit http://localhost:8000 to view the docs

3. **Build documentation:**
   ```bash
   mkdocs build
   ```
   Output will be in the `site/` directory

### Using NPM Scripts

Alternative commands using npm:
```bash
npm run docs:dev      # Start development server
npm run docs:build    # Build documentation
npm run docs:deploy   # Deploy to GitHub Pages
```

## 🎨 Theme & Features

The documentation uses **Material for MkDocs** with the following features:

- **Navigation**: Instant navigation, tabs, sections
- **Search**: Full-text search with suggestions
- **Code**: Syntax highlighting, copy buttons
- **Dark Mode**: Automatic light/dark theme toggle
- **Mobile Responsive**: Works on all devices
- **Edit on GitHub**: Easy contribution links

## 📝 Content Overview

### Core Documentation Files

1. **index.md** - Documentation homepage with quick links
2. **getting-started.md** - Step-by-step guide for new users
3. **faq.md** - Common questions and answers
4. **guides/index.md** - Feature guides and tutorials
5. **guides/best-practices.md** - Best practices and tips
6. **api/index.md** - API reference and integration docs

### Template Links

Many links in the documentation point to pages that don't exist yet. These are placeholders showing where future documentation should go. Examples include:
- API endpoint details
- Individual feature guides
- SDK documentation
- Specific how-to guides

## 🔧 Customization

### Update Site Information

Edit `mkdocs.yml` to customize:
- Site name and description
- Navigation structure
- Theme colors
- Features enabled/disabled

### Add New Pages

1. Create a new `.md` file in the `docs/` directory
2. Add the page to the `nav:` section in `mkdocs.yml`
3. Build and test locally

### Change Theme Colors

In `mkdocs.yml`, modify the `theme.palette` section:
```yaml
theme:
  palette:
    primary: indigo  # Change this
    accent: blue     # Change this
```

## 🤖 Automated Workflows

### CI Workflow (ci.yml)

Runs on pull requests:
- Validates documentation builds without errors
- Checks for broken links (placeholder for linkchecker)
- Uploads preview artifacts

### Deploy Workflow (deploy-docs.yml)

Runs on push to main:
- Builds documentation
- Deploys to GitHub Pages
- Makes docs available at: `https://tradiescribe.github.io/docs-public/`

## 📤 Publishing to GitHub Pages

### First-Time Setup

1. Go to repository Settings → Pages
2. Select "Deploy from a branch"
3. Choose `gh-pages` branch
4. Save

The deploy workflow will automatically create the `gh-pages` branch on first run.

### Manual Deployment

```bash
mkdocs gh-deploy
```

This builds and pushes to the `gh-pages` branch.

## 🤝 Contributing

Contributors can:
- Fix typos and improve existing docs
- Add new documentation pages
- Suggest improvements via issues
- Submit pull requests

See `CONTRIBUTING.md` for detailed guidelines.

## 📚 Next Steps

### Recommended Additions

1. **Add placeholder pages** for linked content:
   - API endpoint details
   - Individual feature guides
   - SDK documentation

2. **Add images and screenshots**:
   - Create `docs/images/` directory
   - Add UI screenshots
   - Include diagrams

3. **Expand API documentation**:
   - Add request/response examples
   - Include error codes and handling
   - Provide SDK examples

4. **Create tutorials**:
   - Step-by-step guides
   - Video content
   - Common use cases

5. **Add search functionality enhancements**:
   - Tags for better organization
   - Custom search index configuration

## 🔍 Documentation Best Practices

1. **Keep it simple**: Use clear, concise language
2. **Use examples**: Include code samples and screenshots
3. **Stay current**: Update docs with product changes
4. **Test links**: Verify all links work before publishing
5. **Get feedback**: Ask users what's missing or confusing

## 🆘 Troubleshooting

### Build Errors

If `mkdocs build` fails:
1. Check for syntax errors in `.md` files
2. Verify all links in `mkdocs.yml` nav are valid
3. Ensure Python dependencies are installed

### Styling Issues

If the site doesn't look right:
1. Clear browser cache
2. Rebuild: `mkdocs build --clean`
3. Check for theme configuration errors

### Deployment Issues

If GitHub Pages deployment fails:
1. Check workflow logs in Actions tab
2. Verify repository permissions
3. Ensure `gh-pages` branch exists

## 📞 Support

For help with this documentation template:
- Open an issue in the repository
- Check MkDocs documentation: https://www.mkdocs.org
- Review Material theme docs: https://squidfunk.github.io/mkdocs-material/

---

**Template Version**: 1.0.0  
**Last Updated**: 2026-01-30  
**Framework**: MkDocs with Material Theme
