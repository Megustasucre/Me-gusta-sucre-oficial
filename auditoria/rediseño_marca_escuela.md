# Auditoría Técnica: Escuela de Español - Aplicación de Marca
**Estado:** 🔴 REQUIERE REDISEÑO VISUAL
**Referencia:** Manual de Marca y Color Flexible **Coral (#FF3B6B)**.

## 1. Sistema de Color "Academia Boutique"
Se debe abandonar el marrón oscuro para dar paso a la claridad y energía de la escuela.

*   **Fondo Global:** Blanco Puro (`#FFFFFF`).
*   **Color de Acento:** Coral (`#FF3B6B`).
*   **Color de Soporte:** Negro Puro (`#000000`) para textos y botones secundarios.
*   **Decoración:** Rosa Empolvado (`#FFDCDC`) para números de sección y marcas de agua.

---

## 2. Ajustes Críticos en Secciones

### A. Stats Bar (Unificación)
Actualmente mezcla Coral y Turquesa.
*   **Acción:** Cambiar todos los números gigantes a **Coral (#FF3B6B)**.
*   **Fondo:** Cambiar fondo marrón (`#1a120a`) por **Rosa Empolvado (#FFDCDC)** con opacidad suave o Blanco.

### B. Sección "El Valor" (Split)
*   **Fondo:** Cambiar `var(--cream)` por **Blanco**.
*   **Iconos:** Los checks de las listas deben ser **Coral**.
*   **Titulares:** Eliminar `font-style: italic` del acento "a life in Spanish".

### C. Sección Precios
*   **Fondo:** Cambiar `var(--dark)` (marrón/negro) por **Negro Puro (#000000)**.
*   **Cards:** Las tarjetas deben ser minimalistas con bordes en **Coral**.

---

## 3. Tipografía y Estilo
1.  **Cero Itálicas:** Todos los títulos `h1`, `h2`, `h3` en Aztec Beat deben ser rectos (`font-style: normal`).
2.  **Mayúsculas:** Forzar `text-transform: uppercase` en todos los titulares de cursos y modalidades.
3.  **Botones:** Unificar `.school-btn-teal` a `.btn-black` (Negro Jalqa) para que el Coral sea el único protagonista cromático.

---
**Auditor:** Senior Technical Auditor
**Objetivo:** Que la Escuela se sienta vibrante, académica y 100% Me Gusta Sucre.
**Fecha:** 12 de Mayo de 2026
