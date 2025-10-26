# Agile Softwareentwicklung - Präsentation

Eine interaktive Präsentation über agile Softwareentwicklung, erstellt mit [reveal.js](https://revealjs.com/).

## 📋 Übersicht

Diese Präsentation bietet eine umfassende Einführung in agile Methoden und Praktiken:
- Grundlagen und Geschichte der agilen Softwareentwicklung
- Das Agile Manifest und seine Prinzipien
- Scrum Framework (Rollen, Events, Artefakte)
- Kanban Methode
- Best Practices und Tools

**Dauer:** ca. 60 Minuten

## 🌐 Live Demo

Die Präsentation ist live verfügbar unter:

**[https://rostigerloeffel.github.io/agile/](https://rostigerloeffel.github.io/agile/)**

Die Präsentation wird automatisch bei jedem Push auf den `main` Branch via GitHub Actions deployed.

## 🚀 Schnellstart

### Voraussetzungen

- [Node.js](https://nodejs.org/) (Version 14 oder höher)
- npm (wird mit Node.js installiert)

### Installation

1. Repository klonen oder herunterladen
2. Abhängigkeiten installieren:
   ```bash
   npm install
   ```

### Präsentation starten

```bash
npm start
```

Die Präsentation öffnet sich automatisch im Browser unter `http://localhost:8080`.

## 📁 Projektstruktur

```
agile/
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Actions Deployment-Workflow
├── css/
│   └── custom.css      # Benutzerdefinierte Styles
├── images/             # Bilder und Grafiken
├── node_modules/       # NPM Abhängigkeiten (nach Installation)
├── index.html          # HTML-Container (lädt slides.md)
├── slides.md           # Präsentations-Inhalt in Markdown
├── package.json        # Projekt-Konfiguration
├── .nojekyll           # Deaktiviert Jekyll auf GitHub Pages
├── README.md           # Diese Datei
├── CLAUDE.md           # Entwickler-Guidelines
└── LICENSE             # Lizenz
```

## ✍️ Inhalte bearbeiten

### Präsentations-Inhalte

Alle Präsentationsinhalte befinden sich in der Datei **`slides.md`** (Markdown-Format).

**Neue Slide hinzufügen:**
```markdown
---

## Meine neue Slide

- Bullet Point 1
- Bullet Point 2
```

**Vertikale Slides (Sub-Slides):**
```markdown
--

### Sub-Slide

Weitere Details zum Thema
```

**Speaker Notes hinzufügen:**
```markdown
## Slide Titel

Sichtbarer Inhalt

Note:
Diese Notizen sind nur im Speaker View (Taste 'S') sichtbar
```

**Slide-Hintergründe:**
```markdown
<!-- .slide: data-background="#2196F3" -->

## Slide mit blauem Hintergrund
```

**Code-Blöcke:**
```markdown
## Code Beispiel

```javascript
function example() {
    return "Hello World";
}
`` `
```
(Ohne Leerzeichen vor den Backticks)

**Bilder einfügen:**
```markdown
![Beschreibung](images/bild.png)
```

### Markdown-Syntax

Die Präsentation verwendet Standard-Markdown mit reveal.js Erweiterungen:
- `---` trennt horizontale Slides
- `--` trennt vertikale Slides
- `Note:` leitet Speaker Notes ein
- `<!-- .slide: ... -->` für Slide-spezifische Attribute

Vollständige Dokumentation: [reveal.js Markdown](https://revealjs.com/markdown/)

## 🎨 Anpassungen

### Theme ändern

In `index.html` das Theme in Zeile 12 anpassen:
```html
<link rel="stylesheet" href="node_modules/reveal.js/dist/theme/black.css" id="theme">
```

Verfügbare Themes: `black`, `white`, `league`, `beige`, `sky`, `night`, `serif`, `simple`, `solarized`, `blood`, `moon`

### Eigene Styles

Benutzerdefinierte Styles können in `css/custom.css` hinzugefügt werden.

### Bilder hinzufügen

Bilder im `images/` Ordner ablegen und in der Präsentation referenzieren:
```html
<img src="images/beispiel.png" alt="Beschreibung">
```

## ⌨️ Tastatur-Shortcuts

- **Pfeiltasten** - Navigation
- **F** - Vollbild
- **S** - Notizen-Ansicht (Speaker Notes)
- **O** - Übersicht aller Slides
- **ESC** - Zoom zurücksetzen
- **B** oder **.** - Bildschirm schwarz schalten
- **?** - Hilfe anzeigen

## 📤 Export

### Als PDF exportieren

1. Präsentation im Browser öffnen
2. `?print-pdf` an die URL anhängen: `http://localhost:8080?print-pdf`
3. Drucken-Dialog öffnen (Strg+P / Cmd+P)
4. Als PDF speichern

### Automatisches Deployment (GitHub Pages)

Dieses Projekt ist für automatisches Deployment auf GitHub Pages konfiguriert:

1. **Automatisch**: Bei jedem Push auf `main` wird die GitHub Action `.github/workflows/deploy.yml` ausgelöst
2. **Build-Prozess**: Dependencies werden installiert (`npm ci`)
3. **Deployment**: Alle Dateien werden als Artifact hochgeladen und deployed
4. **Live-URL**: Die Präsentation ist dann verfügbar unter `https://rostigerloeffel.github.io/agile/`

**Erstmalige Einrichtung:**
Nach dem ersten Push müssen Sie GitHub Pages in den Repository-Einstellungen aktivieren:
- Settings → Pages → Source: **"GitHub Actions"** (nicht Branch!)

### Manuelles Deployment

Die Präsentation kann auch manuell auf anderen Plattformen gehostet werden:
- Alle Dateien (inkl. `node_modules/reveal.js`) hochladen
- `index.html` über Webserver ausliefern
- Alternative Plattformen: Netlify, Vercel, Azure Static Web Apps

## 🛠️ Entwicklung

### Reveal.js Konfiguration

Die Konfiguration befindet sich in `index.html` im `<script>` Tag am Ende:
```javascript
Reveal.initialize({
    hash: true,
    controls: true,
    progress: true,
    // weitere Optionen...
});
```

Alle Optionen: https://revealjs.com/config/

### Plugins

Aktivierte Plugins:
- **Markdown** - Markdown-Unterstützung in Slides
- **Highlight** - Syntax-Highlighting für Code
- **Notes** - Speaker Notes
- **Zoom** - Zoom-Funktion (Alt+Click)
- **Search** - Suche (Strg+Shift+F)

## 📚 Ressourcen

- [Reveal.js Dokumentation](https://revealjs.com/)
- [Agile Manifesto](https://agilemanifesto.org/)
- [Scrum Guide](https://scrumguides.org/)

## 📝 Lizenz

Siehe [LICENSE](LICENSE) Datei für Details
