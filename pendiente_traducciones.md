# Traducciones guia.html — Completado
_Auditado: 2026-05-08 · Implementado: 2026-05-09_

Todo implementado. No quedan items pendientes.

---

## Alta prioridad — DONE

### Las Crónicas (blog index) — 15 items con data-i18n + 1 hardcoded intencional

| Elemento | Clave | Nota |
|---|---|---|
| Tag artículo destacado | `guia.cronSchoolPill` | Reutilizada (ya existía) |
| Título artículo destacado | `guia.cronSchoolTitle` | Reutilizada |
| Excerpt artículo destacado | `guia.cronSchoolDesc` | Reutilizada |
| Meta "8 MIN · 2026" | — | Hardcoded intencional (no es traducible) |
| Tag barrios | `guia.cronBarTag` | Nueva clave EN/ES/FR |
| Título barrios | `guia.cronBarTitle` | Nueva clave EN/ES/FR |
| Excerpt barrios | `guia.cronBarDesc` | Nueva clave EN/ES/FR |
| Tag gastronomia | `guia.cronGasTag` | Nueva clave EN/ES/FR |
| Título gastronomia | `guia.cronGasTitle` | Nueva clave EN/ES/FR |
| Excerpt gastronomia | `guia.cronGasDesc` | Nueva clave EN/ES/FR |
| Tag festividades | `guia.cronFesTag` | Nueva clave EN/ES/FR |
| Título festividades | `guia.cronFesTitle` | Nueva clave EN/ES/FR |
| Excerpt festividades | `guia.cronFesDesc` | Nueva clave EN/ES/FR |
| Tag insider tips | `guia.cronInsTag` | Nueva clave EN/ES/FR |
| Título insider tips | `guia.cronInsTitle` | Nueva clave EN/ES/FR |
| Excerpt insider tips | `guia.cronInsDesc` | Nueva clave EN/ES/FR |
| Tag el manual | `guia.cron5Tag` | Reutilizada |
| Título el manual | `guia.cron5Title` | Reutilizada |
| Excerpt el manual | `guia.cron5Desc` | Reutilizada |

---

## Media prioridad — DONE

### Must-see spots — eyebrows de categoría (9 items)

| Clave | Spot |
|---|---|
| `guia.must1Cat` | Plaza 25 de Mayo |
| `guia.must2Cat` | Casa de la Libertad |
| `guia.must3Cat` | Recoleta |
| `guia.must4Cat` | Catedral |
| `guia.must5Cat` | USFX Derecho |
| `guia.must6Cat` | Cal Orck'o |
| `guia.must7Cat` | ASUR |
| `guia.must8Cat` | San Felipe Neri |
| `guia.must9Cat` | Iglesia San Francisco |

### Los Capítulos — header (2 items)

| Clave | Elemento |
|---|---|
| `guia.chapEyebrow` | "La Guía" / "The Guide" / "Le Guide" |
| `guia.chapTitleWord1` | "Los" / "The" / "Les" |
| `guia.chapTitleWord2` | "Capítulos" / "Chapters" / "Chapitres" |

---

## Baja prioridad — DONE

### Quick Facts bar — labels (4 items)
Tenían `data-i18n` en el HTML pero faltaban las claves en translations.js. Corregido.

| Clave | Texto EN |
|---|---|
| `guia.qf1Label` | "Altitude" |
| `guia.qf2Label` | "Founded" |
| `guia.qf3Label` | "UNESCO Listed" |
| `guia.qf4Label` | "Sunny days / year" |

### Social Proof — labels (3 items)

| Clave | Texto EN |
|---|---|
| `guia.spLabel1` | "Google Rating" |
| `guia.spLabel2` | "Students from 50+ countries" |
| `guia.spLabel3` | "Years in Sucre" |

### About Sucre — badge flotante (1 item)

| Clave | Nota |
|---|---|
| `guia.aboutBadgeBottom` | `data-i18n-html` (contiene `<br>`) |

---

## Extras aplicados en la misma sesión

### hospedaje.html — texto base desactualizado
Dos elementos con texto hardcodeado que no coincidía con la traducción activa:
- `heroSub`: "Una casa colonial..." → "Un hostal de construcción nueva..."
- `narrativeTitleHtml`: "Una casa colonial hecha hogar" → "Comodidad y calma, en el corazón de Sucre"

### index.html + style.css — auditoría SEO/Performance
- `og:image` y `twitter:image`: SVG → PNG (compatible con todas las plataformas)
- `ld+json logo`: SVG → PNG
- `<link rel="preload">` para hero image (mejora LCP)
- H1 con `<span class="sr-only">` para keywords SEO
- Inn image: `width="800" height="520"` (prevención de CLS)
- WhatsApp float: `aria-label="Contactar por WhatsApp"`
- `.ticker-track { will-change: transform }` en style.css
- `.sr-only` definida en style.css (no venía de Tailwind)
