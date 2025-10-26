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
├── index.html          # Haupt-Präsentationsdatei
├── css/
│   └── custom.css      # Benutzerdefinierte Styles
├── images/             # Bilder und Grafiken
├── node_modules/       # NPM Abhängigkeiten (nach Installation)
├── package.json        # Projekt-Konfiguration
├── README.md           # Diese Datei
├── CLAUDE.md           # Entwickler-Guidelines
└── LICENSE             # Lizenz
```

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

### Für Deployment

Die Präsentation kann direkt auf einem Webserver gehostet werden:
- Alle Dateien (inkl. `node_modules/reveal.js`) hochladen
- `index.html` über Webserver ausliefern

Alternative: GitHub Pages, Netlify, Vercel

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
