# Me Gusta Sucre — Estado del proyecto
_Actualizado: 2026-05-07_

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

### Blog pendiente
- **blog-dia-de-campo.html** — excursiones desde Sucre: Cal Orcko, Maragua, Tarabuco, Chataquila. En pausa hasta tener informacion local del usuario.

### Opcional / Futuro
- **Ticker en index.html** — dice "SPANISH CLASSES · HOSTAL · CAFE" — revisar si el termino HOSTAL funciona visualmente o si conviene ajustar
- **Hospedaje.html** — evaluar si agregar seccion de cronicas/blog (actualmente solo guia.html la tiene)

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
- js/translations.js — sistema multilingue EN/ES/FR con data-i18n
- Sin framework, sin build step para HTML
- Fuentes: Fraunces (titulos) + Plus Jakarta Sans (cuerpo) + Sacramento (cursiva decorativa)
