# Blueprint de Lujo Editorial: City Guide (guia.html)
**Estado:** 🔴 REQUIERE REFINAMIENTO DE ÉLITE
**Objetivo:** Eliminar el aspecto genérico y convertir la página en una publicación de diseño.

## 1. Reglas Innegociables de Estética
*   **CERO CURSIVAS:** Eliminar `font-style: italic` de todos los elementos HTML y clases CSS. La marca es SÓLIDA.
*   **CERO SOMBRAS:** Sustituir sombras suaves por bordes finos de **1px solid rgba(0,0,0,0.1)** o nada.
*   **TEXTO MAYÚSCULO:** Todo lo que use **Aztec Beat** debe ser `text-transform: uppercase`.

---

## 2. El Manifiesto "Luxury Letter" (L158)
Rediseñar el bloque del Manifiesto para que se sienta como una carta física:
```css
.manifest-section {
  background: var(--pink) !important;
  padding: 160px 24px; /* Mucho más aire */
}
.manifest-text {
  font-family: 'Inter', sans-serif;
  font-size: 1.25rem; /* Más grande */
  line-height: 2.2; /* Mucho más espaciado */
  max-width: 680px;
  text-align: left;
  letter-spacing: -0.01em;
  columns: 1; /* Mantener columna única para intimidad */
}
.manifest-sig-name {
  font-family: 'Aztec Beat', serif;
  text-transform: uppercase;
  font-size: 2.5rem;
}
```

---

## 3. Quick Facts Bar "Museum Style" (L231)
Convertir la barra en un infográfico minimalista:
```html
<div style="background:#ffffff; border-top:1px solid #FFDCDC; border-bottom:1px solid #FFDCDC; padding:60px 0">
  <!-- Números en Negro Puro, Etiquetas en Rosa Empolvado Sólido -->
  <span style="font-family:'Aztec Beat'; font-size:4rem; color:#000">2810</span>
  <span style="font-family:'Inter'; font-weight:700; color:#FFDCDC; letter-spacing:3px">ALTITUDE</span>
</div>
```

---

## 4. Unificación de los Capítulos (L176)
Los capítulos no deben ser "cartas" con sombras. Deben ser bloques de imagen puros con tipografía superpuesta minimalista.
*   **Acción:** Eliminar `box-shadow` de `.chapter-card`.
*   **Acción:** Asegurar que el número de capítulo (`01`, `02`) sea masivo pero con opacidad muy baja (`0.05`).

---

## 5. El "Cross-sell" Final (L608)
Unificar las tarjetas de productos para que no parezcan anuncios:
*   **Fondo:** Todo a **Negro Puro (#000000)**.
*   **Botones:** Usar la clase `.btn-outline` pero con los colores de marca (Coral/Verde/Blanco) solo en el borde.

---
**Auditor:** Senior Technical Auditor
**Veredicto:** Si aplicamos estos cambios, la Guía pasará de ser "una página de información" a ser **"una declaración de principios"** de Me Gusta Sucre.
