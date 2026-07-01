# Corporate Identity — Andreas Sadlowski
> Abgeleitet von rheumafrei.de · Gültig für alle andreas-sadlowski.de-Seiten

---

## Marke & Ton

- **Person:** Andreas Sadlowski — Autor, Gesundheitsexperte, Schöpfer der KSG H+ Methode
- **Ton:** Vertrauenswürdig, direkt, empathisch. Keine Übertreibungen. Echte Ergebnisse, klare Sprache.
- **Zielgruppe:** Menschen mit chronischen Beschwerden (Rheuma, Schmerzen), 40–70 Jahre, deutschsprachig

---

## Farben

```css
--teal:     #0F766E   /* Primärfarbe — Buttons, Icons, Akzente */
--teal-700: #115E59   /* Dunkleres Teal — Hover, Links */
--teal-50:  #ECFDF5   /* Sehr helles Teal — Hintergründe, Tags */

--ink:      #0B1F1C   /* Fast-Schwarz — Fließtext, Headings */
--ink-2:    #1F2937   /* Etwas heller — Subtext */
--muted:    #4B5563   /* Grau — Beschreibungen, Metainfos */
--line:     #E5E7EB   /* Trennlinien, Borders */

--bg:       #FFFFFF   /* Haupthintergrund */
--bg-2:     #F6FAF9   /* Alternativer Abschnittshintergrund */
--bg-3:     #0B1F1C   /* Dunkler Hintergrund — Header Dark, Footer */

--cta:      #F97316   /* Call-to-Action Orange — Hauptbutton */
--cta-700:  #EA580C   /* Hover-Zustand CTA */

--gold:     #D4A017   /* Akzent — Ribbons, Auszeichnungen */
--rose:     #E11D48   /* Akzent — Warnungen, Preisstreichen */
```

---

## Typografie

| Rolle       | Font            | Gewicht  | Größe (clamp)                    |
|-------------|-----------------|----------|----------------------------------|
| Headlines   | **Lora** (Serif)| 700      | H1: `clamp(1.7rem, 3.6vw, 2.8rem)` |
|             |                 |          | H2: `clamp(1.5rem, 3.2vw, 2.4rem)` |
|             |                 |          | H3: `clamp(1.15rem, 1.7vw, 1.4rem)` |
| Fließtext   | **Inter** (Sans)| 400–700  | `1rem` / `line-height: 1.55`    |
| Eyebrows    | Inter           | 700      | `0.78rem`, `letter-spacing: .14em`, Uppercase |

**Google Fonts Import:**
```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&family=Lora:ital,wght@0,500;0,700;1,500&display=swap">
```

---

## Abstände & Layout

```css
--radius:    14px    /* Standard Rundung */
--radius-lg: 22px    /* Karten, Hero-Elemente */
--maxw:      1160px  /* Max-Breite Container */

.container { max-width: 1160px; margin: 0 auto; padding: 0 22px; }
section    { padding: 80px 0; }
```

**Breakpoints:**
- Mobile-first
- `760px` — 2-spaltige Grids
- `820px` — Footer-Grid, Trustbar
- `880px–980px` — Author-Block, Hero
- `920px` — Desktop-Nav, Sticky-CTA verschwindet
- `1040px` — 3-spaltige Grids

---

## Schatten

```css
--shadow-sm: 0 1px 2px rgba(11,31,28,.06), 0 2px 8px rgba(11,31,28,.04)
--shadow:    0 10px 30px rgba(11,31,28,.08), 0 2px 8px rgba(11,31,28,.04)
--shadow-lg: 0 30px 80px rgba(11,31,28,.18)
```

---

## Komponenten

### Button
```html
<a href="#" class="btn">Text <span class="arrow">→</span></a>
<a href="#" class="btn btn--lg">Groß</a>
<a href="#" class="btn btn--ghost">Ghost</a>
<a href="#" class="btn btn--teal">Teal</a>
<a href="#" class="btn btn--pulse">Pulsierend</a>
```

### Eyebrow (Abschnitts-Label)
```html
<span class="eyebrow">Label</span>
```
Kleiner grüner Chip mit Punkt davor, uppercase.

### Karten
```html
<div class="cards cols-3">
  <div class="card">
    <div class="ico"><!-- SVG --></div>
    <h3>Titel</h3>
    <p>Text</p>
  </div>
</div>
```

### Trustbar (Kennzahlen-Leiste)
```html
<div class="trustbar">
  <div class="container">
    <div class="row">
      <div class="cell"><div class="num">10.000+</div><div class="lbl">Beschreibung</div></div>
    </div>
  </div>
</div>
```

### Testimonial
```html
<div class="t-card">
  <div class="t-tag">Kategorie</div>
  <div class="t-stars">★★★★★</div>
  <p class="t-quote">Zitat</p>
  <div class="t-meta">
    <div class="t-avatar">AB</div>
    <div><div class="t-name">Name</div><div class="t-condition">Diagnose</div></div>
  </div>
</div>
```

### FAQ
```html
<div class="faq">
  <details>
    <summary>Frage?</summary>
    <div class="answer"><p>Antwort</p></div>
  </details>
</div>
```

### Header (Sticky)
```html
<header class="header">
  <div class="container">
    <div class="row">
      <a href="/" class="logo">
        <div class="mark">AS</div>
        Andreas Sadlowski
      </a>
      <nav class="nav">
        <a href="/ueber/">Über mich</a>
        <a href="/blog/">Blog</a>
      </nav>
      <a href="#cta" class="btn">Jetzt starten</a>
      <button class="burger">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
  <nav class="mobile-nav" id="mobileNav">
    <a href="/ueber/">Über mich</a>
  </nav>
</header>
```

### Footer (Dark)
```html
<footer>
  <div class="container">
    <div class="row">
      <div><!-- Brand --></div>
      <div><!-- Nav Links --></div>
      <div><!-- Rechtliches --></div>
    </div>
    <div class="small">© 2025 Andreas Sadlowski · ...</div>
  </div>
</footer>
```

---

## HTML-Seitengerüst (Template)

```html
<!doctype html>
<html lang="de">
<head>
  <!-- Cookiebot -->
  <script id="Cookiebot" src="https://consent.cookiebot.com/uc.js" data-cbid="CBID-HIER" type="text/javascript" async></script>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
  <title>Seitentitel | Andreas Sadlowski</title>
  <meta name="description" content="...">
  <link rel="canonical" href="https://www.andreas-sadlowski.de/SEITE/">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&family=Lora:ital,wght@0,500;0,700;1,500&display=swap">
  <link rel="stylesheet" href="/assets/css/site.css">
</head>
<body>
  <!-- Header -->
  <!-- Sections -->
  <!-- Footer -->
  <script>
    // Mobile Nav Toggle
    document.querySelector('.burger').addEventListener('click', () => {
      document.getElementById('mobileNav').classList.toggle('open');
    });
  </script>
</body>
</html>
```

---

## Assets-Struktur

```
andreas-sadlowski/
├── assets/
│   ├── css/
│   │   └── site.css        ← Kopie/Adaption von rheumafrei
│   ├── js/
│   │   └── (optional)
│   └── img/
│       ├── favicon-32.png
│       ├── favicon-180.png
│       └── favicon-512.png
├── index.html
├── ueber/
│   └── index.html
└── ci.md                   ← Diese Datei
```

---

## Unterschiede zu rheumafrei.de

| Aspekt        | rheumafrei.de            | andreas-sadlowski.de       |
|---------------|--------------------------|----------------------------|
| Fokus         | Produkt (Buch, Methode)  | Person (Autorität, Brand)  |
| Logo-Kürzel   | `RF`                     | `AS`                       |
| Domain        | rheumafrei.de            | andreas-sadlowski.de       |
| Primärfarbe   | Teal (identisch)         | Teal (identisch)           |
| Schriften     | Lora + Inter             | Lora + Inter               |
