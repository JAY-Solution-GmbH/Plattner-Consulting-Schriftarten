# Plattner Consulting Schriftarten

Dieses Repository stellt die drei maßgeschneiderten Schriftarten für Plattner Consulting bereit, optimiert für die Integration in Webprojekte (z. B. **onepage.io**) über ein schnelles, weltweites Content Delivery Network (CDN - jsDelivr).

## Enthaltene Schriftarten
1. **Futura Book** (`fonts/futura-book.woff2` / `.otf`)
2. **Futura Condensed Medium** (`fonts/futura-condensed-medium.woff2` / `.ttf`)
3. **Owners Bold** (`fonts/owners-bold.woff2` / `.ttf`)

---

## Integration in onepage.io

Um diese Schriftarten in Ihrem **onepage.io**-Projekt zu verwenden, folgen Sie bitte diesen einfachen Schritten:

### Schritt 1: Stylesheet im `<head>` einbinden
Fügen Sie im Einstellungsbereich Ihres onepage.io-Projekts unter **„Custom Code“** (oder **„Header-Code“**) die folgende Zeile ein:

```html
<!-- Plattner Consulting Custom Fonts -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/JAY-Solution-GmbH/Plattner-Consulting-Schriftarten@main/fonts.css">
```

### Schritt 2: Schriftarten im CSS anwenden
Mit folgendem CSS-Code definieren wir **Futura Book** als Standard-Schriftart für alle Elemente der Seite (einschließlich aller Paragraphen, Listen, Span-Tags und Divs). Anschließend überschreiben wir diese gezielt für **H1, H2 und H3 Überschriften** (inklusive ihrer verschachtelten Elemente), damit diese in **Owners Bold** dargestellt werden.

Verwenden Sie dazu folgende CSS-Definitionen:

```css
/* 1. Futura Book für absolut alle Elemente auf der Seite festlegen */
* {
  font-family: 'Futura Book', sans-serif !important;
}

/* 2. H1, H2 und H3 Überschriften (und alle Elemente darin) auf Owners Bold setzen */
h1, h2, h3,
h1 *, h2 *, h3 * {
  font-family: 'Owners Bold', sans-serif !important;
  font-weight: bold !important;
}

/* 3. Optionale Klasse für Futura Condensed Medium */
.schmale-ueberschrift, .schmale-ueberschrift * {
  font-family: 'Futura Condensed Medium', sans-serif !important;
}
```

---

## Funktionsweise & CDN-Caching
Die Schriftarten werden über die GitHub-Repository-Dateien direkt an das **jsDelivr-CDN** weitergeleitet. Dadurch ist sichergestellt, dass:
* Die Ladezeiten minimal sind (dank globalem Edge-Caching).
* Korrekte CORS-Header (`Access-Control-Allow-Origin: *`) gesendet werden, was Browser-Sicherheitsfehler beim Laden der Schriftart verhindert.
