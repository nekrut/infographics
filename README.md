# Galaxy Infographics

A collection of promotional HTML pages for the Galaxy Project, served via GitHub Pages.

## View Online

**https://nekrut.github.io/infographics/**

## Available Infographics

| Directory | Description | View |
|-----------|-------------|------|
| `what_is_galaxy/` | Interactive slideshow introducing Galaxy (14 slides) | [View](what_is_galaxy/) |
| `what_is_brc/` | Interactive slideshow introducing BRC Analytics (12 slides) | [View](what_is_brc/) |
| `vgp/` | VGP on Galaxy - Vertebrate Genomes Project (9 slides) | [View](vgp/) |

## Generating Content

Infographics are generated using the [infographics-generator](https://github.com/nekrut/infographics-generator) framework.

### Workflow

1. **Edit content** in the generator repository:
   ```bash
   cd ~/git/infographics-generator/sites/<site_name>
   # Edit slides.md with your content
   ```

2. **Build the HTML**:
   ```bash
   cd ~/git/infographics-generator
   node build.js sites/<site_name>
   ```

3. **Deploy to this repository**:
   ```bash
   cp -r ~/git/infographics-generator/sites/<site_name>/dist ~/git/infographics/<site_name>
   ```

4. **Commit and push**:
   ```bash
   cd ~/git/infographics
   git add .
   git commit -m "Update <site_name>"
   git push
   ```

### Framework Location

The infographics-generator framework:
```
~/git/infographics-generator/
├── build.js           # Build script
├── template.html      # Default HTML template
└── sites/
    ├── what_is_galaxy/
    │   ├── slides.md      # Content source
    │   └── images/        # Site images
    ├── what_is_brc/
    │   ├── slides.md
    │   ├── template.html  # Custom BRC template
    │   └── images/
    └── vgp/
        ├── slides.md
        └── images/
```

## Adding New Infographics

1. Create a new site in the generator:
   ```bash
   mkdir -p ~/git/infographics-generator/sites/new_site/{images,dist}
   ```

2. Create `slides.md` with your content

3. Optionally create a custom `template.html` for different branding

4. Build and deploy as described above

5. Update this README and `index.html` to list the new site

## GitHub Pages

This repository is served via GitHub Pages at:
```
https://nekrut.github.io/infographics/
```

Each infographic is accessible at:
```
https://nekrut.github.io/infographics/<directory_name>/
```

## Controls

All slideshows support:

| Key | Action |
|-----|--------|
| `Space` | Pause / Resume |
| `→` | Next slide |
| `←` | Previous slide |
