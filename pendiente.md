# Me Gusta Sucre — Estado del proyecto
_Actualizado: 2026-05-07 (sesion 2)_

---

## Lo que se hizo

### Correcciones globales de marca
- **Me Gusta Inn** (no "Inn — Boutique Hotel" ni "Boutique Hotel"): reemplazado en los 13 archivos HTML del sitio (footers, cards, CTAs)
- **Me Gusta Escuela** (no "Me Gusta Spanish School" en texto visible): verificado
- Confirmado que `translations.js` ya tenia los valores correctos (brand2Pill: "Hostal", brand2Name: "Me Gusta Sucre Inn")
- **clases.html** — stat "3 Native Teachers" cambiado a "100%" (practicamente todos los profesores son nativos)

### Blogs completados (6 de 7)

| Archivo | Tema | CTA | Estado |
|---|---|---|---|
| blog-aprende-espanol.html | Por que aprender espanol en Sucre | Escuela | Completo |
| blog-el-manual.html | Manual del viajero (transporte, plata, seguridad) | Inn | Completo |
| blog-insider-tips.html | 10 secretos locales | Cafe | Completo |
| blog-gastronomia.html | Salteñas, mercado, chorizos, cafes, api | Cafe | Completo |
| blog-festividades.html | Carnaval, Pujllay, Semana Santa, Dia de Muertos, Guadalupe | Inn | Completo |
| blog-barrios.html | La Recoleta, Centro, La Glorieta, Parque Bolivar, Peatonizacion | Inn | Completo |

### Correcciones de contenido en blogs existentes
- **blog-el-manual.html**: micro Bs 1.50 → Bs 3 / taxi min Bs 3 → Bs 7 / eliminada referencia a Policia Turistica (no existe)
- **blog-aprende-espanol.html**: fixed related links (eliminado blog-tradiciones-domingo.html que no existe)
- **blog-insider-tips.html**: CTA cambiado de Inn a Cafe (mas coherente con el contenido)
- **blog-gastronomia.html**: descripcion de chorizo completamente reescrita (EN PLATO: ensalada + pan sopado en jugo / EN SANDWICH)

### guia.html — Las Cronicas
- Blog destacado: blog-aprende-espanol.html
- Side list (5 cards): barrios, gastronomia, festividades, insider-tips, el-manual
- Eliminadas referencias a blogs inexistentes (blog-tradiciones-domingo.html, blog-sucre-after-dark.html)

### Auditoria UX/SEO completada (sesion 2)
- **Blogs EN/ES/FR**: sistema `data-lang-block` — los 5 blogs (barrios, gastronomia, festividades, insider-tips, aprende-espanol) ahora tienen contenido en los 3 idiomas. Cada seccion tiene bloque EN/ES/FR; se muestra el activo segun el idioma seleccionado.
- **Precios USD en hospedaje.html**: referencia en USD bajo cada habitacion ($42 privada bano privado / $28 privada bano compartido / $55 familiar / $12 dorm)
- **CLS fix**: width y height agregados a todos los `<img>` en 13 archivos
- **guia.html — auditoria completa**: los 13 items del audit resueltos (fondos, border-radius, breadcrumb, quick facts, pro tip, modal SVG, social proof, hero font-size, contadores carrusel, logos, z-index, i18n refactor, sticky filters)
- **Mobile menu "Book a Stay"**: movido arriba del selector de idioma en todos los archivos
- **Touch targets mobile**: links del menu mobile de py-2 → py-3 (cumple minimo 44px) en 14 archivos
- **Logo duplicado en mobile**: eliminado el bloque de logo dentro del `#mobile-menu` en 13 archivos — ya no se duplica al abrir el hamburguesa
- **translations.js minificado**: 186KB → 165KB (11% menos)
- **js/main.js**: agregado soporte para `data-lang-block` (show/hide por idioma)

### Hechos verificados con investigacion
- **La Glorieta**: Francisco Argandona + Clotilde Urioste, construido 1893-1897, arquitecto Camponovo, estilo eclectico, Papa Leon XIII otorgo titulo de Principe 1898, unico principado de Sudamerica
- **Torre en Parque Bolivar**: observatorio meteorologico disenado por firma Eiffel en 1906, trasladado al parque en 1925 para el centenario de Bolivia. No hay conexion documentada con Argandona.
- **Pujllay Tarabuco**: tercer domingo de marzo, conmemora batalla de Jumbati 1816
- **Heladeria Sandra**: fundada en 1966, ubicada en Parque Bolivar

---

## Pendientes

### Alta prioridad
1. ~~**URL oficial del cafe**~~ — Actualizado a https://www.megustaspanish.com/cafe (2026-05-07)
2. ~~**Menu del cafe con precios**~~ — El menu vive en megustaspanish.com/cafe, al cual apuntan los CTAs (2026-05-07)
3. ~~**Blogs en ingles para usuarios EN/FR**~~ — Resuelto con sistema data-lang-block (2026-05-07)
4. ~~**Mobile "Book a Stay" oculto**~~ — Movido arriba del selector de idioma (2026-05-07)
5. ~~**Precios USD en hospedaje**~~ — Agregados como referencia bajo cada habitacion (2026-05-07)
6. ~~**CLS — width/height en imagenes**~~ — Resuelto en 13 archivos (2026-05-07)

### Requiere decision del cliente
- **Motor de reservas**: sistema actual (formulario → WhatsApp) tiene friccion para turistas internacionales. Opciones: Cloudbeds, Sirvoy, Little Hotelier (todos tienen widget embeddable). Mantener WhatsApp como canal secundario.
- **Formulario de contacto**: contacto.html solo tiene WhatsApp/tel/mailto. Usuario en desktop sin cliente de correo no puede contactar. Opcion simple: FormSubmit o Netlify Forms.

### Blog pendiente
- **blog-dia-de-campo.html** — excursiones desde Sucre: Cal Orcko, Maragua, Tarabuco, Chataquila. En pausa hasta tener informacion local del usuario.

### Opcional / Futuro
- **Ticker en index.html** — dice "SPANISH CLASSES · HOSTAL · CAFE" — revisar si el termino HOSTAL funciona visualmente o si conviene ajustar
- **Hospedaje.html** — evaluar si agregar seccion de cronicas/blog (actualmente solo guia.html la tiene)
- **Refactor estilos inline** — deuda tecnica: muchos `style="..."` inline en el HTML. Migracion gradual a clases CSS. Baja prioridad.
- **og:image PNG** — exportar imagenes/og-image.svg a PNG 1200x630 para previews de WhatsApp/Facebook

---

## Estructura del sitio

| Archivo | Descripcion |
|---|---|
| index.html | Homepage con ticker, hero, cards de las 3 marcas |
| clases.html | Me Gusta Escuela — cursos de espanol |
| hospedaje.html | Me Gusta Inn — hostal La Paz #571 |
| cafe.html | Me Gusta Cafe — Bolivar #603 |
| guia.html | Guia de Sucre + Las Cronicas (blog index) |
| contacto.html | Pagina de contacto con 3 cards (Inn, Cafe, Escuela) |
| merchandising.html | Merch — remeras, tote bags, tazas |
| blog-aprende-espanol.html | Blog |
| blog-el-manual.html | Blog |
| blog-insider-tips.html | Blog |
| blog-gastronomia.html | Blog |
| blog-festividades.html | Blog |
| blog-barrios.html | Blog |

## Stack tecnico
- HTML estatico + Tailwind (css/tw.css) + css/style.css + css/sucre-fonts.css
- js/translations.js — sistema multilingue EN/ES/FR con data-i18n (minificado, 165KB)
- js/main.js — navbar scroll, mobile menu, i18n, data-lang-block support
- Sin framework, sin build step para HTML
- Fuentes: Fraunces (titulos) + Plus Jakarta Sans (cuerpo) + Sacramento (cursiva decorativa)
- Sistema de idiomas blogs: `data-lang-block="en/es/fr"` — show/hide por idioma activo
