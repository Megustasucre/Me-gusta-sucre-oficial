# review.md — Me Gusta Sucre · Estado del Proyecto

> Documento de referencia actualizado. Revisar antes de hacer cambios significativos.
> Última actualización: 2026-05-02

---

## Estado general

Sitio web estático multilingüe (EN / ES / FR) desplegado en GitHub Pages en **megustasucre.com**.
Stack: HTML / CSS / Vanilla JS — sin framework, sin backend.

### Páginas activas

| Página | Estado | Notas |
|---|---|---|
| `index.html` | Estable | Hero landing, trust bar, 4 brand cards, atracciones, reviews marquee |
| `hospedaje.html` | Revisado y completo | Ver sección detallada abajo |
| `guia.html` | Estable | City guide editorial con scroll-spy nav, bento grid, carousels, blog |
| `cafe.html` | Teaser | Menú 8 items, sección atmósfera. Pendiente: rediseño completo |
| `clases.html` | Teaser | 4 programas, links a megustaspanish.com. Pendiente: rediseño |
| `contacto.html` | Estable | 3 tarjetas de ubicación (Escuela / Inn / Café) |
| `merchandising.html` | Funcional | Productos, gift coupons, carrito via `js/merch-cart.js` |
| `404.html` | Estable | Trilingüe, animación chinchilla pixel-art |
| `blog-el-manual.html` | Publicado | Blog standalone |
| `blog-aprende-espanol.html` | Publicado | Blog standalone |
| `blog-post.html` | Template | Plantilla para futuros posts |

---

## hospedaje.html — Estado completo (2026-05-02)

### Diseño
Rediseño completo implementado. Secciones:
1. **Hero** — imagen `vista_terraza.webp`, booking bar (arrival / departure / guests / CTA)
2. **Narrative** — texto + imagen entrada, badges de ubicación
3. **Rooms** — 4 tarjetas (Private/Private Bath, Private/Shared Bath, Family, Dorm)
4. **Amenities** — 8 celdas en grid 2 columnas mobile / 4 desktop
5. **Cross-sell** — banners Café y Escuela con imágenes locales
6. **Gallery** — grid asimétrico 4 fotos
7. **Booking form** — room selector, fechas, resumen sticky, envío por WhatsApp
8. **CTA** — sección final con imagen terraza

### i18n
- Todas las claves en EN / ES / FR (60+ claves hospedaje)
- Chips de habitaciones: `chipPrivateBath`, `chipHotWater`, `chipFiberWifi`, etc.
- Botón: `btnReserve` (EN: "Select →", ES: "Reservar →", FR: "Réserver →")
- Unidades: `unitNight`, `sumLabelPrice`
- Toggle estudiante: `studentToggleText`, `studentToggleBadge`

### Copy
- Edificio **nuevo y moderno** — sin referencias a "colonial" ni "siglo XIX"
- Foco: tranquilidad, comodidad, mejor ubicación de Sucre
- Voz: "Anfitrión Experto" — cálido, directo, sin lenguaje turístico
- Nombres de habitaciones ES corregidos (eran legacy del diseño anterior)

### Performance
- Hero image preload (LCP): `vista_terraza.webp`
- `loading="lazy"` en 9 imágenes below-fold
- Script order: `translations.js` antes que `main.js`
- Sin Google Fonts duplicado (usa `sucre-fonts.css`)
- Imágenes WebP optimizadas: ~5.7 MB total (antes: ~20 MB)

### Imágenes usadas (hostal/)
| Archivo | Peso | Uso |
|---|---|---|
| `hostal_general/vista_terraza.webp` | 424 KB | Hero background |
| `baño_privado/DSC08147-HDR-2.webp` | 540 KB | Room 1 card |
| `baño_compartido/DSC08217-HDR.webp` | 531 KB | Room 2 card |
| `familiar/DSC08332-HDR.webp` | 602 KB | Room 3 card |
| `seis_camas/DSC08489-HDR.webp` | 381 KB | Dorm card |
| `hostal_general/Entrada.webp` | 276 KB | Narrative |
| `hostal_general/terraza_3.webp` | 440 KB | Gallery |
| `hostal_general/area_compartida_1.webp` | 620 KB | Gallery |
| `hostal_general/pasillo_1.webp` | 340 KB | Gallery |
| `hostal_general/area_compartida_2.webp` | 662 KB | Gallery |
| `baño_privado/DSC08172-HDR-2.webp` | 692 KB | Booking summary thumb |

### Precios actuales (Bs)
| Habitación | Normal | Descuento estudiante (17%) |
|---|---|---|
| Privada c/ Baño Privado | 230 Bs | 150 Bs (1p) / 190 Bs (2p) |
| Privada c/ Baño Compartido | 180 Bs | 130 Bs (1p) / 150 Bs (2p) |
| Familiar | 365 Bs | 300 Bs / noche |
| Dorm (por cama) | 103 Bs | 85 Bs / cama |

---

## Sistema i18n

- Archivo: `js/translations.js` (~2500 líneas)
- Estructura: `translations.{lang}.{section}.{key}`
- HTML: `data-i18n="section.key"` (textContent) / `data-i18n-html="section.key"` (innerHTML)
- Idioma: URL param `?lang=es` o `localStorage.mgs_lang`
- **Importante:** las secciones hospedaje tienen claves duplicadas en ES y FR (legacy de versiones anteriores). La última clave del objeto es la que prevalece en JS.

---

## CSS / Design System

Archivo base: `css/style.css`

### Variables globales
```css
--red: #c9252d       /* brand global */
--gold: #e8a020      /* merch */
--dark: #1a1a2e
--cream: #faf8f4
```

### Override por producto (inline en cada página)
```css
--teal: #14b8a6      /* Inn / hospedaje */
--school: #FF3B6B    /* Escuela */
--cafe-green: #5aaa6a /* Café */
```

### Clases clave
`.fade-up` · `.eyebrow` · `.section-luxury` · `.hero-kenburns` · `.btn-red` · `.btn-gold`

---

## Pendiente / Próximas prioridades

### Alta prioridad
- [ ] Push a GitHub (4 commits locales sin publicar — push estaba fallando)
- [ ] `cafe.html` — rediseño completo al mismo nivel que `hospedaje.html`
- [ ] `clases.html` — rediseño completo

### Media prioridad
- [ ] `index.html` — revisar consistencia de copy con el nuevo posicionamiento del Inn
- [ ] Revisar translations.js: limpiar claves duplicadas en hospedaje ES/FR (legacy)
- [ ] `merchandising.html` — revisar estado y actualizar precios si cambiaron

### Baja prioridad
- [ ] Más artículos de blog
- [ ] `contacto.html` — verificar horarios y datos actualizados

---

## Git

- Remote: `https://github.com/Megustasucre/me-gusta-sucre.git`
- Branch: `master`
- Deploy: GitHub Pages → megustasucre.com

```bash
# Publicar cambios pendientes
git push origin master

# Build Tailwind (si se edita tw-input.css)
npm run build:css
```

---

## Notas técnicas

- **No usar emojis** en HTML/CSS. Usar texto uppercase, SVG o abreviaciones.
- **Tipografía:** Fraunces (headings) + Plus Jakarta Sans (body). Sacramento solo decorativo.
- **Imágenes nuevas:** siempre WebP, comprimir a <600 KB para cards, <400 KB para thumbs, <300 KB para hero.
- **`tw.css` nunca editar directo** — regenerar con `npm run build:css` tras editar `tw-input.css`.
- **Python build scripts** (`build_carousels.py`, etc.) — ejecutar manualmente cuando se actualiza contenido editorial de guia/blog.
