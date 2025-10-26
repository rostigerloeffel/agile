# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains an interactive presentation about **Agile Software Development** built with reveal.js. The presentation is designed for approximately 60 minutes and covers fundamental agile concepts, methodologies (Scrum, Kanban), and best practices.

## Technology Stack

- **reveal.js 5.1.0** - HTML presentation framework
- **Node.js** - Runtime environment
- **live-server** - Development server with auto-reload
- **HTML5/CSS3** - Markup and styling
- **JavaScript** - Presentation configuration and interactivity

## Project Structure

```
agile/
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Actions CI/CD pipeline
├── css/
│   └── custom.css      # Custom styles and theme overrides
├── images/             # Presentation images and graphics
├── node_modules/       # Dependencies (installed via npm)
│   └── reveal.js/      # Reveal.js framework
├── index.html          # Main presentation file (all slides)
├── package.json        # NPM configuration
├── .nojekyll           # Prevents Jekyll processing on GitHub Pages
├── README.md           # User documentation
└── CLAUDE.md           # This file - developer guidance
```

## Development Workflow

### Setup and Installation
```bash
npm install         # Install dependencies (reveal.js, live-server)
npm start           # Start development server on port 8080
```

### File Organization

**index.html**
- Contains all presentation slides in `<section>` elements
- Nested `<section>` elements create vertical slide stacks
- reveal.js configuration at the bottom of the file
- Uses German language (`lang="de"`)

**css/custom.css**
- Custom color scheme using CSS variables
- Responsive utilities (two-column layouts, etc.)
- Helper classes for info boxes, highlights
- Image and code block styling
- Override reveal.js defaults here

**images/**
- Store all presentation images here
- Reference in slides: `<img src="images/filename.png" alt="description">`

## Reveal.js Key Concepts

### Slide Structure
```html
<!-- Horizontal slide -->
<section>
    <h2>Title</h2>
    <p>Content</p>
</section>

<!-- Vertical slide stack -->
<section>
    <section>Main topic</section>
    <section>Sub-topic 1</section>
    <section>Sub-topic 2</section>
</section>
```

### Speaker Notes
```html
<section>
    <h2>Slide Title</h2>
    <p>Visible content</p>
    <aside class="notes">
        These notes are only visible in speaker view (press 'S')
    </aside>
</section>
```

### Configuration Options (index.html)
Key settings in `Reveal.initialize()`:
- `hash: true` - URL reflects current slide
- `width/height` - Presentation dimensions
- `controls/progress` - UI elements
- `transition` - Slide transition effect
- `plugins` - Enabled features

## Content Guidelines

### Presentation Theme
- **Topic**: Agile Software Development
- **Duration**: ~60 minutes
- **Language**: German
- **Target audience**: Developers/teams learning agile methods

### Content Sections (Planned)
1. Introduction to Agile
2. Agile Manifest (values & principles)
3. Scrum Framework (roles, events, artifacts)
4. Kanban Method
5. Best Practices & Tools
6. Q&A

### Slide Best Practices
- Keep text concise (bullet points preferred)
- Use vertical stacks for related sub-topics
- Add speaker notes for additional context
- Include visuals where helpful (diagrams, charts)
- Use custom CSS classes for emphasis (`.highlight`, `.info-box`, etc.)

## Common Tasks

### Adding New Slides
1. Locate appropriate section in index.html
2. Add new `<section>` element
3. Include title, content, and optionally speaker notes
4. Test navigation flow

### Changing Theme
Modify line 12 in index.html:
```html
<link rel="stylesheet" href="node_modules/reveal.js/dist/theme/THEME_NAME.css">
```
Available themes: black, white, league, beige, sky, night, serif, simple, solarized, blood, moon

### Adding Images
1. Place image in `images/` directory
2. Reference in slide:
```html
<img src="images/example.png" alt="Description">
```

### Custom Styling
Add to `css/custom.css`:
- New color schemes (update CSS variables)
- Layout utilities
- Animation overrides
- Font customizations

### Export to PDF
1. Add `?print-pdf` to URL: `http://localhost:8080?print-pdf`
2. Open print dialog (Ctrl+P / Cmd+P)
3. Save as PDF

## Keyboard Shortcuts (Presenter)
- Arrow keys - Navigate slides
- `S` - Speaker notes view
- `O` - Overview mode
- `F` - Fullscreen
- `B` / `.` - Pause (black screen)
- `?` - Help overlay

## Deployment & CI/CD

### GitHub Pages Deployment

The project uses GitHub Actions for automated deployment to GitHub Pages.

**Live URL**: https://rostigerloeffel.github.io/agile/

### GitHub Actions Workflow

**File**: `.github/workflows/deploy.yml`

**Trigger**: Automatically runs on every push to `main` branch

**Workflow Steps**:
1. **Checkout**: Pulls latest code from repository
2. **Setup Node.js**: Installs Node.js v20 with npm caching
3. **Install Dependencies**: Runs `npm ci` to install reveal.js and dependencies
4. **Setup Pages**: Configures GitHub Pages environment
5. **Upload Artifact**: Uploads entire project directory as artifact
6. **Deploy**: Deploys artifact to GitHub Pages using official action

**Key Configuration**:
```yaml
permissions:
  contents: read   # Read repository contents
  pages: write     # Write to GitHub Pages
  id-token: write  # Write ID tokens for deployment

environment:
  name: github-pages  # Uses GitHub Pages environment
```

**Deployment Method**: Uses official GitHub Actions workflow (artifact-based deployment), NOT branch-based deployment.

### First-Time Setup

After the first push, GitHub Pages must be enabled in repository settings:

1. Navigate to repository **Settings** → **Pages**
2. Set **Source** to: **"GitHub Actions"** (NOT a branch!)
3. Save changes (if not already set)
4. Re-run the workflow if needed (Actions tab)
5. GitHub will deploy automatically (takes 1-2 minutes)
6. Presentation will be available at the GitHub Pages URL

### Deployment Process

Every push to `main` triggers:
1. GitHub Actions workflow starts
2. Dependencies are installed (cached for speed)
3. All project files (including `node_modules/reveal.js/`) are packaged as an artifact
4. Artifact is deployed to GitHub Pages environment
5. GitHub Pages automatically serves the updated presentation

**Deployment Time**: Typically 1-3 minutes from push to live

**Note**: This uses artifact-based deployment, not branch-based. No `gh-pages` branch is created.

### .nojekyll File

The `.nojekyll` file in the root directory is crucial:
- Prevents GitHub Pages from processing files with Jekyll static site generator
- Without it, directories starting with `_` (like `node_modules/reveal.js/dist/_includes`) would be ignored
- Ensures reveal.js assets load correctly

### Local Testing Before Deployment

Always test locally before pushing:
```bash
npm install  # Ensure dependencies are installed
npm start    # Test presentation at http://localhost:8080
```

### Troubleshooting Deployment

**Problem**: Workflow fails with "git failed with exit code 128"
- **Check**: Repository settings → Settings → Pages → Source must be **"GitHub Actions"**
- **Solution**: Change source from branch-based to GitHub Actions, re-run workflow

**Problem**: Presentation shows 404 or broken assets
- **Check**: Ensure GitHub Pages source is set to "GitHub Actions" in settings
- **Check**: Verify workflow completed successfully in Actions tab
- **Solution**: Wait 2-3 minutes after push for deployment to complete

**Problem**: Styles/scripts not loading
- **Check**: `.nojekyll` file exists in root
- **Check**: Workflow completed successfully (check Actions tab)
- **Solution**: Hard refresh browser (Ctrl+F5), check console for errors

**Problem**: Workflow fails during upload/deployment step
- **Check**: Repository settings → Pages is enabled
- **Check**: Workflow has correct permissions (pages:write, id-token:write)
- **Solution**: Ensure Pages is enabled and source is set to "GitHub Actions"

**Problem**: Changes not visible on live site
- **Check**: GitHub Actions tab for workflow status (must show green checkmark)
- **Check**: Browser cache (hard refresh with Ctrl+F5)
- **Solution**: Wait for workflow completion (1-3 min), clear browser cache

### Manual Deployment Alternative

To manually deploy to other platforms (Netlify, Vercel, etc.):
1. Run `npm install` locally
2. Upload entire project directory (including `node_modules/reveal.js/`)
3. Set build command: `npm install` (if platform supports it)
4. Set publish directory: `./` (root)

## Important Notes

- All dependencies are local (no CDN) - works offline after `npm install`
- Changes to HTML/CSS auto-reload when using `npm start`
- Speaker notes are hidden from audience, visible only in presenter view
- Presentation can be deployed as static files (no server-side processing needed)
- GitHub Actions deployment is fully automated - just push to `main`

## Future Enhancements

Potential improvements:
- Add presenter timer/clock
- Include multimedia (video demos)
- Interactive code examples
- Real-time polls/quizzes
- Additional plugins (charts, math equations)
