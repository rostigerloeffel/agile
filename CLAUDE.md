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
├── slides/             # Modular presentation content (Markdown)
│   ├── 01-intro.md         # Introduction & History (~10 min)
│   ├── 02-manifest.md      # Agile Manifest (~8 min)
│   ├── 03-scrum.md         # Scrum Framework (~16 min)
│   ├── 04-kanban.md        # Kanban (~10 min)
│   ├── 05-frameworks.md    # Other Frameworks (XP, SAFe, LeSS) (~5 min)
│   ├── 06-best-practices.md # Best Practices & Antipatterns (~8 min)
│   └── 07-outro.md         # Q&A & Resources (~3 min)
├── node_modules/       # Dependencies (installed via npm)
│   └── reveal.js/      # Reveal.js framework
├── index.html          # HTML container (loads slides/*.md)
├── slides.md           # [DEPRECATED] Old monolithic file (kept as backup)
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

**slides/ Directory** ⭐ PRIMARY CONTENT LOCATION
- **Modular structure:** Content split into 7 separate Markdown files
- Each file represents one section of the presentation (~60 minutes total)
- Files are loaded sequentially by index.html via reveal.js Markdown plugin
- Markdown syntax (same for all files):
  - Horizontal slides separated by `---`
  - Vertical slides (sub-slides) separated by `--`
  - Speaker notes start with `Note:`
  - Slide attributes via HTML comments: `<!-- .slide: data-background="#color" -->`

**File Breakdown:**
1. `01-intro.md` - Introduction, history, Why Agile? (~10 min)
2. `02-manifest.md` - 4 Values, 12 Principles, misconceptions (~8 min)
3. `03-scrum.md` - Roles, Events, Artefacts with examples (~16 min)
4. `04-kanban.md` - Visualization, WIP Limits, Flow (~10 min)
5. `05-frameworks.md` - XP, SAFe, LeSS (~5 min)
6. `06-best-practices.md` - Technical Excellence, DO's/DON'Ts, Antipatterns (~8 min)
7. `07-outro.md` - Q&A, Resources, Takeaways (~3 min)

**index.html**
- Minimal HTML container with 7 `<section>` tags (one per file)
- Each section loads from `slides/XX-name.md`
- Contains reveal.js configuration at the bottom
- Uses German language (`lang="de"`)
- DO NOT add slide content here - use files in `slides/` directory

**css/custom.css**
- Custom color scheme using CSS variables
- Responsive utilities (two-column layouts, etc.)
- Helper classes for info boxes, highlights
- Image and code block styling
- Override reveal.js defaults here

**images/**
- Store all presentation images here
- Reference in slides.md: `![Alt text](images/filename.png)`

## Markdown-Based Workflow

### Slide Structure in slides.md

**Horizontal Slides** (separated by `---`):
```markdown
# First Slide

Content here

---

## Second Slide

More content

---

## Third Slide

Even more content
```

**Vertical Slides** (sub-slides, separated by `--`):
```markdown
## Main Topic

Introduction to the topic

--

### Sub-Topic 1

Details about first aspect

--

### Sub-Topic 2

Details about second aspect

---

## Next Main Topic

Back to horizontal navigation
```

Navigation:
- Left/Right arrows: Horizontal slides
- Up/Down arrows: Vertical slides (if present)

### Speaker Notes
```markdown
## Slide Title

Visible content that audience sees

Note:
These notes are only visible in speaker view (press 'S').
Multiple lines are supported.
Great for talking points and reminders.
```

### Slide Attributes

**Background Colors:**
```markdown
<!-- .slide: data-background="#2196F3" -->

## Slide with Blue Background

Content here
```

**Background Images:**
```markdown
<!-- .slide: data-background="images/background.jpg" -->

## Slide with Image Background
```

**Multiple Attributes:**
```markdown
<!-- .slide: data-background="#FF5722" data-transition="zoom" -->

## Special Slide

With custom background and transition
```

### Markdown Syntax

**Headings:**
```markdown
# H1 (usually for title slides)
## H2 (main slide titles)
### H3 (sub-headings)
```

**Lists:**
```markdown
- Bullet point 1
- Bullet point 2
  - Nested item
  - Another nested item

1. Numbered item
2. Another numbered item
```

**Emphasis:**
```markdown
*italic text*
**bold text**
***bold italic***
~~strikethrough~~
```

**Links:**
```markdown
[Link Text](https://example.com)
```

**Images:**
```markdown
![Alt text](images/diagram.png)
```

**Code Blocks:**
````markdown
```javascript
function example() {
    return "Hello World";
}
```
````

Supported languages: javascript, python, java, css, html, bash, etc.

**Inline Code:**
```markdown
Use `code` for inline code snippets.
```

**Blockquotes:**
```markdown
> This is a quote
> Spanning multiple lines
```

**Tables:**
```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |
| Data 4   | Data 5   | Data 6   |
```

### Configuration Options (index.html)
Key settings in `Reveal.initialize()`:
- `hash: true` - URL reflects current slide
- `width/height` - Presentation dimensions (1280x720)
- `controls/progress` - UI elements
- `transition` - Slide transition effect ('slide', 'fade', 'zoom', etc.)
- `plugins` - Enabled features (Markdown, Highlight, Notes, Zoom, Search)

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
1. Open `slides.md`
2. Add separator `---` for new horizontal slide
3. Write content using Markdown syntax
4. Optionally add `Note:` section for speaker notes
5. Save and refresh browser (auto-reloads with live-server)

Example:
```markdown
---

## New Slide Title

- Point 1
- Point 2
- Point 3

Note:
Remember to mention the key takeaway here
```

### Adding Vertical Slides (Sub-Slides)
1. Use `--` separator instead of `---`
2. These create a vertical stack under the current horizontal slide

Example:
```markdown
## Main Topic

Overview

--

### Detail 1

First detail

--

### Detail 2

Second detail

---

## Next Main Topic
```

### Changing Theme
Modify line 12 in index.html:
```html
<link rel="stylesheet" href="node_modules/reveal.js/dist/theme/THEME_NAME.css">
```
Available themes: black, white, league, beige, sky, night, serif, simple, solarized, blood, moon

### Adding Images
1. Place image in `images/` directory
2. Reference in slides.md:
```markdown
![Image Description](images/example.png)
```

For custom sizing, use HTML:
```markdown
<img src="images/example.png" alt="Description" width="600">
```

### Adding Code Examples
Use fenced code blocks with language identifier:
````markdown
```python
def greet(name):
    return f"Hello, {name}!"
```
````

### Custom Slide Backgrounds
Add before slide content:
```markdown
<!-- .slide: data-background="#FF5722" -->

## Slide with Orange Background
```

### Custom Styling
Add to `css/custom.css`:
- New color schemes (update CSS variables)
- Layout utilities
- Animation overrides
- Font customizations

### Using Custom CSS Classes
In slides.md:
```markdown
<div class="info-box">
This is an info box with custom styling
</div>
```

Available custom classes (see `css/custom.css`):
- `.info-box` - Blue info box
- `.success-box` - Green success box
- `.warning-box` - Orange warning box
- `.highlight` - Highlighted text
- `.two-columns` - Two-column layout

### Export to PDF
1. Add `?print-pdf` to URL: `http://localhost:8080?print-pdf`
2. Open print dialog (Ctrl+P / Cmd+P)
3. Save as PDF

### Testing Changes
1. Run `npm start`
2. Edit `slides.md`
3. Save file
4. Browser auto-reloads (thanks to live-server)
5. No manual refresh needed!

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

- **Primary content file**: `slides.md` (Markdown format) - ALL slide content goes here
- **DO NOT edit slides in index.html** - it only loads slides.md
- All dependencies are local (no CDN) - works offline after `npm install`
- Changes to slides.md/CSS auto-reload when using `npm start`
- Speaker notes are hidden from audience, visible only in presenter view (press 'S')
- Presentation can be deployed as static files (no server-side processing needed)
- GitHub Actions deployment is fully automated - just push to `main`
- Markdown syntax is faster and cleaner than HTML for content creation

## Future Enhancements

Potential improvements:
- Add presenter timer/clock
- Include multimedia (video demos)
- Interactive code examples
- Real-time polls/quizzes
- Additional plugins (charts, math equations)
