# IMMO Integration Layer - Datenfluss Visualisierung

Eine interaktive Visualisierung der Systemlandschaft für das IMMO Integration Layer Projekt des Bundesamts für Bauten und Logistik (BBL).

## 🚀 Live Demo

[Hier klicken für die Live-Demo](https://[dein-github-username].github.io/immo-graph/)

## 📋 Übersicht

Diese Visualisierung zeigt:
- **21 Systeme** der BBL-Systemlandschaft
- **6 externe Datenquellen** (BFS, Kantone, etc.)
- **15 BBL-Kernsysteme** (SAP, Fachsysteme, Dokumente)
- **Über 50 Datenflüsse** mit unterschiedlichen Kritikalitätsstufen

## 🎯 Features

### Interaktive Funktionen
- **Klicken** auf Knoten zeigt detaillierte Systeminformationen
- **Doppelklick** fokussiert auf ein System
- **Drag & Drop** zum Neuanordnen der Knoten
- **Zoom** mit Mausrad oder Touch-Gesten

### Filter & Layouts
- **Layout-Optionen**: Hierarchisch, Physik-basiert, Kreisförmig
- **Kategorie-Filter**: Nach Systemtyp filtern
- **Kritikalitäts-Filter**: Nach Datenfluss-Priorität filtern
- **Export-Funktion**: Netzwerkdaten als JSON exportieren

### Farbkodierung

| Farbe | Kategorie | Beschreibung |
|-------|-----------|--------------|
| 🟨 Gelb | Data Owner | Datenverantwortliche Organisationen |
| 🔵 Hellblau | Externe Systeme | Datenquellen außerhalb BBL |
| 🟢 Grün | SAP ERP | SAP-Kernmodule |
| 🟠 Orange | Fachsysteme | Spezialisierte Anwendungen |
| 🟣 Lila | Dokumente | DMS und Archive |
| 🌸 Rosa | Visualisierung | GIS und BIM Systeme |

### Linientypen (Kritikalität)

| Linientyp | Priorität | Beschreibung |
|-----------|-----------|--------------|
| Dicke rote Linie | Hoch | Kritische Real-time Verbindungen |
| Normale blaue Linie | Mittel | Wichtige Batch-Prozesse |
| Gestrichelte graue Linie | Niedrig | Optionale/seltene Transfers |

## 📁 Projektstruktur

```
immo-graph/
├── index.html          # Hauptseite mit Visualisierung
├── data.json           # Netzwerkdaten (Knoten & Kanten)
└── README.md           # Diese Datei
```

## 🛠️ Technologie-Stack

- **[vis.js Network](https://visjs.github.io/vis-network/docs/network/)** - Netzwerk-Visualisierung
- **Vanilla JavaScript** - Keine zusätzlichen Frameworks
- **HTML5 & CSS3** - Moderne Web-Standards
- **GitHub Pages** - Hosting

## 📊 Datenstruktur

### Knoten (Nodes)
```json
{
  "id": "B1",
  "label": "SAP RE-FX",
  "group": "sapERP",
  "color": "#90EE90",
  "title": "Immobilienstammdaten",
  "dataOwner": "BBL",
  "status": "Produktiv",
  "prioritaet": "MUSS"
}
```

### Kanten (Edges)
```json
{
  "from": "E1",
  "to": "B1",
  "label": "EGID/EWID",
  "color": "#FF0000",
  "width": 4,
  "priority": "high",
  "arrows": "to",
  "title": "API, Täglich, Kritikalität: Hoch"
}
```

## 🚀 Installation & Deployment

### Lokale Entwicklung
1. Repository klonen
2. `index.html` im Browser öffnen
3. Fertig!

### GitHub Pages Deployment

1. Repository auf GitHub erstellen
2. Dateien hochladen:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```
3. GitHub Pages aktivieren:
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: main / root
   - Save

## 📝 Daten aktualisieren

1. `data.json` bearbeiten
2. Neue Knoten oder Kanten hinzufügen
3. Commit und push zu GitHub
4. Änderungen sind automatisch live

## 🔧 Anpassungsmöglichkeiten

### Farben ändern
In `index.html` die Farben in der CSS-Section anpassen:
```css
.legend-color {
    background-color: #90EE90; /* Neue Farbe hier */
}
```

### Neue Kategorien hinzufügen
In `data.json`:
1. Neue `group` definieren
2. In HTML Filter-Option hinzufügen
3. Legende erweitern

## 📈 Statistiken

- **Systeme gesamt**: 33 (inkl. Data Owner)
- **Datenflüsse**: 60+
- **Kritische Verbindungen**: 17
- **Mittlere Priorität**: 20
- **Niedrige Priorität**: 11

## 🤝 Mitwirkende

- **Projektleitung**: BBL IMMO Integration Layer Team
- **Datengrundlage**: Studie Visualisierung Datenfluss (Arbeitsdokument)
- **Visualisierung**: Solution Architecture Team

## 📄 Lizenz

Dieses Projekt ist Teil der SUPERB-Initiative der Schweizer Bundesverwaltung.

## 🔗 Verwandte Projekte

- [SBIM-1732](https://jira.admin.ch/browse/SBIM-1732) - SBIM: IMMO Layer Integration/Orchestration
- [SBCOREART-7230](https://jira.admin.ch/browse/SBCOREART-7230) - IMMO Integrationslayer: Datenflüsse
- [SBIM-4739](https://jira.admin.ch/browse/SBIM-4739) - Diagramm & Datenfluss-Matrix

## 📞 Kontakt

Für Fragen und Anregungen wenden Sie sich an das BBL Solution Architecture Team.

---

*Stand: Oktober 2024*
