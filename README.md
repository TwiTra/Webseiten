# Webseiten

Eigene Webseiten. Jeder Push auf `main` prüft das HTML und veröffentlicht automatisch alles aus `sites/` über GitHub Pages.

## Aufbau

```
sites/
  index.html            ← Übersichtsseite mit Karten zu allen Seiten
  meine-seite/          ← ein Ordner pro Webseite
    index.html
    bilder/ …
```

Erreichbar ist jede Seite unter `https://<benutzername>.github.io/webseiten/<ordnername>/`.

## Neue Seite hinzufügen

1. Ordner `sites/<name>/` mit einer `index.html` anlegen (Bilder, CSS, JS daneben).
2. In `sites/index.html` eine Karte kopieren und auf `<name>/` verlinken.
3. Hochladen. Nach 1–2 Minuten ist die Seite online (Reiter **Actions** zeigt den Stand).

## Einmalig einrichten

In GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

> GitHub Pages ist bei **privaten** Repos nur mit GitHub Pro (oder Team) verfügbar. Ohne Pro das Repo auf *öffentlich* stellen oder die Seiten über einen anderen Dienst (z. B. Netlify, Cloudflare Pages) veröffentlichen.

## Lokal prüfen

```bash
npx html-validate "sites/**/*.html"
```
