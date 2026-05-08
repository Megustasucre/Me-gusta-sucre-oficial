# Pendiente — Traducciones guia.html
_Auditado: 2026-05-08_

---

## Alta prioridad

### Las Crónicas (blog index) — 16 items
Todo el bloque está hardcodeado en español. Requiere `data-lang-block` o `data-i18n` para EN/ES/FR.

| Elemento | Texto actual (ES) | Línea |
|---|---|---|
| Tag artículo destacado | "Clases de Español" | ~760 |
| Título artículo destacado | "El secreto mejor guardado para aprender español" | ~761 |
| Excerpt artículo destacado | "El acento mas neutro del continente. Ciudad universitaria desde 1624. Inmersion total a bajo costo." | ~762 |
| Meta artículo destacado | "8 MIN · 2026" | ~763 |
| Tag barrios | "La Ciudad" | ~775 |
| Título barrios | "Sucre contada desde adentro" | ~776 |
| Excerpt barrios | "De La Recoleta al Parque Bolívar — la ciudad en orden histórico..." | ~777 |
| Tag gastronomia | "Gastronomia" | ~786 |
| Título gastronomia | "Lo que hay que comer en Sucre" | ~787 |
| Excerpt gastronomia | "Salteñas con papaya Salvietti, chorizos de 7 Lunares..." | ~788 |
| Tag festividades | "Festividades" | ~797 |
| Título festividades | "Las celebraciones que definen Sucre" | ~798 |
| Excerpt festividades | "Carnaval de antaño, Pujllay de Tarabuco, Semana Santa..." | ~799 |
| Tag insider tips | "Secretos Locales" | ~808 |
| Título insider tips | "10 cosas que solo los locales saben" | ~809 |
| Excerpt insider tips | "Lo que una vida entera en Sucre te enseña..." | ~810 |
| Tag el manual | "El Manual" | ~819 |
| Título el manual | "Todo lo que necesitas saber antes de llegar" | ~820 |
| Excerpt el manual | "Altitud, moneda, transporte, clima y seguridad..." | ~821 |

---

## Media prioridad

### Must-see spots — eyebrows de categoría (9 items)
Labels hardcodeados en inglés encima del título de cada spot, sin `data-i18n`.

| Texto actual (EN) | Spot | Línea |
|---|---|---|
| "Central Square" | Plaza 25 de Mayo | ~360 |
| "Museum" | Casa de la Libertad | ~375 |
| "Viewpoint" | Recoleta | ~389 |
| "Architecture" | Catedral | ~403 |
| "Architecture" | USFX Derecho | ~417 |
| "Dinosaur Park" | Cal Orck'o | ~435 |
| "Museum — Indigenous Textiles" | ASUR | ~450 |
| "Rooftop — Church Towers" | San Felipe Neri | ~465 |
| "Architecture — 1538" | Iglesia San Francisco | ~479 |

### Los Capítulos — header (2 items)

| Texto actual | Idioma | Línea |
|---|---|---|
| "La Guía" | ES (eyebrow) | ~154 |
| "Los Capítulos" | ES (heading) | ~156 |

---

## Baja prioridad

### Quick Facts bar — labels (3 items)

| Texto actual (EN) | Línea |
|---|---|
| "Google Rating" | ~305 |
| "Students from 50+ countries" | ~310 |
| "Years in Sucre" | ~315 |

### About Sucre — badge flotante (1 item)

| Texto actual (EN) | Línea |
|---|---|
| "Year-round sunshine, no crowds." | ~255 |

---

## Notas técnicas

- Las Crónicas: usar `data-lang-block="en/es/fr"` igual que los blogs individuales
- Must-see spots + stats + badge: agregar claves `guia.must1Cat`, `guia.statLabel1`, etc. a translations.js (EN/ES/FR) y `data-i18n` en el HTML
- Los Capítulos header: agregar claves `guia.chapEyebrow` y `guia.chapTitle` a translations.js
