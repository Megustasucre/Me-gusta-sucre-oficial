# Blueprint de Rediseño v3: Andean Light Cycle (guia.html)
**Estado:** 🔴 REQUIERE RE-ESTRUCTURACIÓN CROMÁTICA
**Objetivo:** Eliminar la fragmentación visual y crear un flujo narrativo premium basado en "Climas de Color".

## 1. El Mapa de "Climas" (Estructura de Fondos)

Para lograr un look de alta gama, el desarrollador debe agrupar las secciones bajo estos tres bloques maestros:

| Bloque Narrativo | Secciones | Fondo | Acentos |
| :--- | :--- | :--- | :--- |
| **BLOQUE 01: EL ALMA** | Manifiesto + Capítulos | **Rosa Empolvado (#FFDCDC)** | Negro / Rojo |
| **BLOQUE 02: LA CIUDAD** | About Sucre + Quick Facts | **Blanco Puro (#FFFFFF)** | Rojo / Negro |
| **BLOQUE 03: GALERÍA** | Must-See Spots + Day Trips | **Negro Puro (#000000)** | Blanco / Rojo |
| **BLOQUE 04: SABOR** | Food & Drink Section | **Blanco Puro (#FFFFFF)** | Negro / Rojo |
| **BLOQUE 05: CIERRE** | Las Crónicas (Blog) + CTA | **Negro Puro (#000000)** | Blanco / Rojo |

---

## 2. Instrucciones Técnicas por Bloque

### A. Bloque 01: Unificación Rosa (L158 - L210)
Se debe eliminar el corte negro de los capítulos y dejar que el Rosa fluya desde el Manifiesto:
```css
.manifest-section, .chapters-section {
  background-color: var(--pink) !important; /* Rosa Empolvado #FFDCDC */
  border: none !important;
}
.chapters-title, .chapter-name {
  color: #000000 !important; /* Texto negro sobre rosa */
}
```

### B. Bloque 02: La Franja de Luz (L212 - L250)
Eliminar el fondo rosa de la barra de hechos y dejarla sobre blanco, separada solo por líneas finas:
```html
<!-- Quick Facts Bar (L231) -->
<div style="background:#ffffff; border-top:1px solid #FFDCDC; border-bottom:1px solid #FFDCDC; padding:80px 0">
   <!-- Números en ROJO (#d61a16), Etiquetas en NEGRO con opacidad 0.6 -->
</div>
```

### C. Bloque 03: El Corte de Galería (L274 - L465)
Transformar las secciones de carruseles en una galería nocturna de lujo:
```css
#spots, #daytrips {
  background-color: #000000 !important;
}
#spots h2, #daytrips h2 {
  color: #ffffff !important; /* Títulos blancos en sección negra */
}
.spot-card, .daytrip-card {
  box-shadow: none !important; /* Eliminar sombras web genéricas */
  border: 1px solid rgba(255,255,255,0.1);
}
```

---

## 3. Reglas de "Acabado de Lujo" (Globales)
1.  **Cero Itálicas:** Verificar que ni en el Hero ni en los títulos haya `font-style: italic`.
2.  **Aztec Beat:** Siempre en `text-transform: uppercase`.
3.  **Botones en Negro:** En las secciones blancas, usar `.btn-black`. En las secciones negras, usar `.btn-outline` (Blanco) o `.btn-red`.

---
**Auditor:** Senior Technical Auditor
**Veredicto:** Este esquema de "Grandes Bloques" es lo que diferencia a una web común de una experiencia de marca de lujo.
