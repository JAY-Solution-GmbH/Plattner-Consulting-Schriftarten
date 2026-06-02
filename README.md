# Plattner Consulting Schriftarten

Dieses Repository stellt die drei maßgeschneiderten Schriftarten für Plattner Consulting bereit, optimiert für die Integration in Webprojekte (z. B. **onepage.io**) über ein schnelles, weltweites Content Delivery Network (CDN - jsDelivr).

## Enthaltene Schriftarten
1. **Futura Book** (`fonts/futura-book.otf`) - Format: OpenType (OTF)
2. **Futura Condensed Medium** (`fonts/futura-condensed-medium.ttf`) - Format: TrueType (TTF)
3. **Owners Bold** (`fonts/owners-bold.ttf`) - Format: TrueType (TTF)

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
Sie können die Schriftarten nun in den globalen CSS-Einstellungen oder in benutzerdefinierten CSS-Code-Blöcken auf onepage.io verwenden.

Verwenden Sie dazu die folgenden `font-family`-Definitionen:

#### Für Fließtext (Futura Book):
```css
body, p, span {
  font-family: 'Futura Book', sans-serif !important;
}
```

#### Für kondensierte Überschriften oder Akzente (Futura Condensed Medium):
```css
.schmale-ueberschrift {
  font-family: 'Futura Condensed Medium', sans-serif !important;
}
```

#### Für markante Überschriften (Owners Bold):
```css
h1, h2, h3, .bold-heading {
  font-family: 'Owners Bold', sans-serif !important;
  font-weight: bold;
}
```

---

## Funktionsweise & CDN-Caching
Die Schriftarten werden über die GitHub-Repository-Dateien direkt an das **jsDelivr-CDN** weitergeleitet. Dadurch ist sichergestellt, dass:
* Die Ladezeiten minimal sind (dank globalem Edge-Caching).
* Korrekte CORS-Header (`Access-Control-Allow-Origin: *`) gesendet werden, was Browser-Sicherheitsfehler beim Laden der Schriftart verhindert.
