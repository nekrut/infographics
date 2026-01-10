# Galaxy Infographics

A collection of promotional HTML pages for the Galaxy Project, served via GitHub Pages.

## Available Infographics

| Directory | Description | View |
|-----------|-------------|------|
| `what_is_galaxy/` | Interactive slideshow introducing Galaxy | [View](what_is_galaxy/) |
| `what_is_brc/` | Interactive slideshow introducing BRC Analytics | [View](what_is_brc/) |

**Front page:** https://nekrut.github.io/infographics/

## Generating Content

Infographics are generated using the promo-site framework in the [gxy-reports](https://github.com/nekrut/gxy-reports) repository.

### Workflow

1. **Edit content** in the framework repository:
   ```bash
   cd ~/git/gxy-reports/promo-site
   # Edit slides.md with your content
   ```

2. **Build the HTML**:
   ```bash
   npm install      # First time only
   npm run build    # Generates index.html
   ```

3. **Copy to this repository**:
   ```bash
   # Copy generated files to appropriate directory
   cp index.html ~/git/infographics/<infographic_name>/
   cp -r images ~/git/infographics/<infographic_name>/
   cp favicon.svg ~/git/infographics/<infographic_name>/
   ```

4. **Commit and push**:
   ```bash
   cd ~/git/infographics
   git add .
   git commit -m "Update <infographic_name>"
   git push
   ```

### Framework Location

The promo-site framework is located at:
```
~/git/gxy-reports/promo-site/
├── slides.md       # Content source (edit this)
├── build.js        # Build script
├── template.html   # HTML template with CSS/JS
└── package.json    # Dependencies
```

See the [promo-site README](https://github.com/nekrut/gxy-reports/tree/master/promo-site) for detailed documentation on the markdown format.

## Adding New Infographics

1. Create a new directory in this repository:
   ```bash
   mkdir ~/git/infographics/new_infographic_name
   ```

2. Either:
   - Copy and modify the promo-site framework for a new slideshow
   - Create a standalone HTML file for simpler content

3. Copy the generated/created files to the new directory

4. Update this README to add the new infographic to the table above

## GitHub Pages

This repository is configured to serve via GitHub Pages at:
```
https://nekrut.github.io/infographics/
```

Each infographic is accessible at:
```
https://nekrut.github.io/infographics/<directory_name>/
```

### Setup (one-time)

1. Go to repository Settings → Pages
2. Source: Deploy from branch
3. Branch: `master` (or `main`), folder: `/ (root)`
4. Save

## QR Codes

For conference displays, generate QR codes pointing to the GitHub Pages URLs:
- Use [qr-code-generator.com](https://www.qr-code-generator.com/) or similar
- Example: QR code for `https://nekrut.github.io/infographics/what_is_galaxy/`
