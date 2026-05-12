# Auditoría Técnica: Fondos y Coherencia Cromática - Escuela
**Estado:** 🔴 REQUIERE LIMPIEZA DE COLORES LEGACY
**Objetivo:** Eliminar rastros de marrón y crema para cumplir con el esquema "Gelería Boutique" (Blanco/Rosa/Negro).

## 1. Detección de Fondos Incoherentes (clases.html)

Tras el escaneo del código, estas secciones aún presentan colores que "ensucian" la marca:

### A. Sección de Modalidades (Programs)
*   **Hallazgo:** La clase `.programs-section` (L245) hereda un fondo marrón oscuro `#120904` del CSS (L1804).
*   **Problema:** Este marrón no pertenece a la paleta oficial y compite con el Negro Puro.
*   **Acción:** Cambiar a **Negro Puro (#000000)** para que las tarjetas Coral resalten con fuerza.

### B. Tarjetas de Modalidades (`.school-dark-card`)
*   **Hallazgo:** Las tarjetas usan un fondo `#1c1008` (Marrón chocolate).
*   **Acción:** Cambiar el fondo de las tarjetas a un **Gris casi negro (#111111)** o **Negro Puro (#000000)** con borde Coral.

### C. Sección Galería (Gallery)
*   **Hallazgo:** Usa `background: var(--cream2)` (L298).
*   **Acción:** Cambiar a **Blanco Puro (#FFFFFF)**. El aire entre las fotos debe ser blanco para que la galería se sienta moderna.

### D. Borde de Foto Acento (`.photo-accent`)
*   **Hallazgo:** El borde usa `var(--cream)` (L1837).
*   **Acción:** Cambiar por un borde **Blanco** o eliminarlo para una estética más minimalista.

---

## 2. Recomendación de "Hilo Rosa" en la Escuela

Para que la página no se vea solo "Blanco y Negro", el Rosa Empolvado debe usarse así:

1.  **Stats Bar:** El fondo actual es Rosa (#FFDCDC). Es una buena decisión, pero si se prefiere fondo blanco, el Rosa debe ir en el **borde inferior** de la barra de stats.
2.  **Divisores:** Asegurar que todas las clases `.divider-line` usen el color **Rosa Empolvado**.

---

## 3. Guía de Implementación para Desarrollador (CSS)

```css
/* Limpieza de la Escuela */

.programs-section {
  background: #000000 !important; /* Unificar con la sección de precios */
}

.school-dark-card {
  background: #111111 !important; /* Negro elegante, no marrón */
}

.gallery-section-school {
  background: #ffffff !important; /* Galería limpia */
}

/* Bordes decorativos */
.photo-accent {
  border: 6px solid #ffffff !important; /* Adiós al crema */
}
```

---
**Auditor:** Senior Technical Auditor
**Veredicto:** Una vez eliminados estos marrones, la Escuela será visualmente indistinguible de una academia de diseño de alto nivel.
