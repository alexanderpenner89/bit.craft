# bit.craft

[![Ghost](https://img.shields.io/badge/Ghost-5.x-black)](https://ghost.org)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

> Ghost-Theme für Wissenschaftstransfer ins Handwerk — strukturiert, inhaltsdicht, gewerkenah.

bit.craft ist ein Ghost-Theme das für die Plattform [bit.transfer](https://github.com/alexanderpenner89/bit.transfer) entwickelt wurde. Es richtet sich an gewerkeorientierten Wissenschaftsjournalismus mit klarer Inhaltsstruktur, Sidebar-Navigation und Newsletter-Integration.

## Features

- **Gewerke-Navigation** — Sidebar mit gewerkebasierter Filterung
- **Dossier-Karten** — Kompakte Darstellung thematisch gebündelter Artikel
- **Newsletter-CTA** — Konfigurierbare Anmeldebereiche für gewerk-spezifische Newsletter
- **Post-Karten** — Übersichtliche Beitragsvorschau mit Tag und Metadaten
- **Paginierung** — Seitenweise Navigation durch Beitragsübersichten

## Installation

1. ZIP der aktuellen Version unter [Releases](https://github.com/alexanderpenner89/bit.craft/releases/latest) herunterladen
2. Ghost Admin → Settings → Design → Change theme → ZIP hochladen
3. Theme aktivieren

## Anpassung

Über Ghost Admin → Settings → Design → Customize stehen folgende Optionen zur Verfügung:

| Option | Beschreibung | Standard |
|--------|--------------|---------|
| `Newsletter-Button` | Button-Text im Newsletter CTA | `NEWSLETTER AUSWÄHLEN` |
| `Sidebar-Text` | Text im Sidebar Newsletter-Block | `Forschung direkt ins Postfach…` |

## Dateistruktur

```
bit.craft/
├── assets/
│   ├── css/screen.css     # Styles
│   └── js/app.js          # JavaScript
├── partials/
│   ├── dossier-card.hbs   # Dossier-Karte
│   ├── navigation.hbs     # Sidebar-Navigation
│   ├── pagination.hbs     # Paginierung
│   ├── post-card.hbs      # Beitrags-Karte
│   └── sidebar.hbs        # Sidebar
├── default.hbs            # Basis-Layout
├── index.hbs              # Startseite / Übersicht
├── post.hbs               # Einzelbeitrag
├── page.hbs               # Statische Seite
├── tag.hbs                # Tag-Übersicht
├── error.hbs              # Fehlerseite
└── package.json           # Ghost Theme Konfiguration
```

## Entwicklung

```bash
# Theme lokal mit Ghost testen
docker compose --profile ghost up -d
# Theme-Verzeichnis in Ghost mounten oder ZIP hochladen
```

Änderungen am Theme lösen automatisch einen neuen Release mit aktualisierter ZIP aus (via GitHub Actions).

## Lizenz

MIT — siehe [LICENSE](LICENSE).
