# Blueprint de Rediseño: City Guide (guia.html)
**Estado:** 🔴 REQUIERE IMPLEMENTACIÓN
**Objetivo:** Elevar la Guía de la Ciudad a una pieza editorial de lujo, eliminando el estilo "web antigua" y aplicando el esquema **Blanco / Negro / Rosa**.

## 1. Cambios Estructurales de Color (Ritmo Visual)

| Sección | Nuevo Fondo | Color Texto / Acentos |
| :--- | :--- | :--- |
| **Hero** | Imagen + Gradiente Negro | **Rojo Marca (#D61A16)** |
| **El Manifiesto** | **Rosa Empolvado (#FFDCDC)** | **Negro Puro (#000000)** |
| **Los Capítulos** | **Negro Puro (#000000)** | Blanco / Rojo |
| **About Sucre** | **Blanco Puro (#FFFFFF)** | Negro / Rojo |
| **Quick Facts Bar** | **Rosa Empolvado (#FFDCDC)** | **Negro Puro (#000000)** |
| **Spots & Day Trips**| **Blanco Puro (#FFFFFF)** | Negro / Rojo |
| **CTA Cross-sell** | **Negro Puro (#000000)** | Colores de Sub-marca |

---

## 2. Guía Técnica: Fragmentos de Código

### A. Hero y Títulos (Adiós Italics)
Sustituir el titular del Hero (L146):
```html
<h1 style="font-family:'Aztec Beat',serif; font-size:clamp(2.8rem,5.5vw,4.8rem); text-transform:uppercase; color:#fff; line-height:1.1">
  <span data-i18n="guia.heroTitle">WELCOME TO</span> <br>
  <span style="color:#d61a16; font-style:normal" data-i18n="guia.heroAccent">BOLIVIA'S MOST BEAUTIFUL CITY</span>
</h1>
```

### B. El Manifiesto (Estilo Intimo)
Sustituir estilos de la sección (L158):
```css
.manifest-section {
  background: var(--pink) !important; /* Rosa Oficial */
  padding: 120px 24px;
}
.manifest-text {
  color: #000000;
  opacity: 0.8;
  font-size: 1.1rem;
  line-height: 2;
}
```

### C. Quick Facts (Contraste de Lujo)
Sustituir estilos de la barra (L231):
```html
<div style="background:#FFDCDC; padding:40px 0; border-bottom:1px solid rgba(0,0,0,0.05)">
  <!-- Etiquetas en Negro, Números en Rojo -->
  <span style="color:#d61a16; font-family:'Aztec Beat'; ...">2810m</span>
  <span style="color:#000000; opacity:0.6; font-weight:700; ...">ALTITUDE</span>
</div>
```

### D. Unificación de Cross-sell (CTA Final)
Asegurar que los botones de marca sigan el sistema:
*   **Spanish:** `.mgcard-btn--coral` (#FF3B6B).
*   **Inn:** `.mgcard-btn--black` (#000000).
*   **Café:** `.mgcard-btn--green` (#5aaa6a).

---

## 3. Tipografía y Rigor Visual
1.  **Aztec Beat:** Forzar `text-transform: uppercase` en todos los nombres de capítulos y atracciones.
2.  **Itálicas:** Buscar y eliminar `font-style: italic` o etiquetas `em` en todos los encabezados de sección.
3.  **Líneas:** Todas las `.divider-line` deben ser **Rosa Empolvado (#FFDCDC)**.

---
**Auditor:** Senior Technical Auditor
**Veredicto:** Con este blueprint, la City Guide se convierte en el mejor "vendedor" de la ciudad y de las marcas Me Gusta Sucre.
