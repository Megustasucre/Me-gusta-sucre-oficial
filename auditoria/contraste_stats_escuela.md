# Auditoría Técnica: Contraste y Accesibilidad - Stats Bar
**Estado:** 🔴 REQUIERE AJUSTE DE CONTRASTE
**Referencia:** Usabilidad y Legibilidad de Marca.

## 1. Hallazgo: Conflicto de Contraste
El texto descriptivo de las estadísticas (`Students`, `Teachers`, etc.) se pierde sobre el fondo Rosa Empolvado debido a una opacidad demasiado baja (`0.45`).

## 2. Instrucciones de Corrección (Opción A: Fondo Rosa)
Si se mantiene el fondo Rosa (#FFDCDC), aplicar:
*   **Etiquetas:** Cambiar `rgba(0,0,0,0.45)` por **`#000000`** con opacidad **`0.7`**.
*   **Números:** Mantener **Coral (#FF3B6B)** pero asegurar que la fuente Aztec Beat esté bien definida.

## 3. Instrucciones de Corrección (Opción B: Inversión de Lujo - RECOMENDADO)
Para un look más premium y legible:
*   **Fondo de Barra:** **Negro Puro (#000000)**.
*   **Números gigantes:** **Coral (#FF3B6B)**.
*   **Etiquetas:** **Rosa Empolvado (#FFDCDC)**.
*   *Razón:* El Rosa sobre Negro brilla con elegancia y elimina cualquier problema de lectura.

---
**Auditor:** Senior Technical Auditor
**Veredicto:** La Opción B (Inversa) es la que mejor encaja con el ritmo de "Claro/Oscuro" que propusimos para la página.
