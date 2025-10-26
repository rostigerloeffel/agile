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
├── index.html          # Main presentation file (all slides)
├── css/
│   └── custom.css      # Custom styles and theme overrides
├── images/             # Presentation images and graphics
├── node_modules/       # Dependencies (installed via npm)
│   └── reveal.js/      # Reveal.js framework
├── package.json        # NPM configuration
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

## Important Notes

- All dependencies are local (no CDN) - works offline after `npm install`
- Changes to HTML/CSS auto-reload when using `npm start`
- Speaker notes are hidden from audience, visible only in presenter view
- Presentation can be deployed as static files (no server-side processing needed)

## Future Enhancements

Potential improvements:
- Add presenter timer/clock
- Include multimedia (video demos)
- Interactive code examples
- Real-time polls/quizzes
- Additional plugins (charts, math equations)
