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
Da onepage.io häufig verschachtelte Tags (wie `<span>` innerhalb von Überschriften) verwendet, müssen die CSS-Regeln robust geschrieben sein, damit globale Text-Styles nicht die Überschriften überschreiben.

Verwenden Sie dazu folgende CSS-Definitionen:

#### 1. Für Überschriften (Owners Bold):
Dieser Selektor stellt sicher, dass alle Überschriften (inklusive eventueller innerer `<span>`-Elemente) korrekt mit Owners Bold dargestellt werden.
```css
h1, h2, h3, h4, h5, h6,
h1 *, h2 *, h3 *, h4 *, h5 *, h6 * {
  font-family: 'Owners Bold', sans-serif !important;
  font-weight: bold !important;
}
```

#### 2. Für Fließtext (Futura Book):
Wendet Futura Book auf allen Fließtext an, schließt aber Überschriften und deren Kinder explizit aus.
```css
body, p, li, a, .op-text, .op-paragraph,
span:not(h1 *, h2 *, h3 *, h4 *, h5 *, h6 *) {
  font-family: 'Futura Book', sans-serif !important;
}
```

#### 3. Für kondensierte Akzente (Futura Condensed Medium):
Wird für gezielte Textelemente verwendet, z. B. über eine eigene Klasse.
```css
.schmale-ueberschrift, .schmale-ueberschrift * {
  font-family: 'Futura Condensed Medium', sans-serif !important;
}
```

---

## Funktionsweise & CDN-Caching
Die Schriftarten werden über die GitHub-Repository-Dateien direkt an das **jsDelivr-CDN** weitergeleitet. Dadurch ist sichergestellt, dass:
* Die Ladezeiten minimal sind (dank globalem Edge-Caching).
* Korrekte CORS-Header (`Access-Control-Allow-Origin: *`) gesendet werden, was Browser-Sicherheitsfehler beim Laden der Schriftart verhindert.
