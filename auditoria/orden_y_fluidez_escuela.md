# Auditoría Técnica: Re-ordenamiento y Fluidez - Escuela
**Estado:** 🔴 REQUIERE RE-ESTRUCTURACIÓN
**Objetivo:** Lograr un ritmo visual "Claro - Oscuro - Claro" que guíe al usuario sin fatiga.

## 1. Nuevo Mapa de Estructura (clases.html)

Se debe mover el bloque de código para seguir este orden de lectura:

1.  **HERO** (Actual)
2.  **SPLIT INTRO** (Mover aquí): Fondo Blanco. La historia de Fernando y Ely debe ir primero para conectar emocionalmente.
3.  **STATS BAR** (Mover aquí): Fondo Rosa Empolvado. Funciona como un "intermedio" visual.
4.  **PROGRAMS (MODALIDADES)**: Cambiar a Fondo **Blanco**. Presentar las clases presenciales y online con mucha luz.
5.  **PRICING**: Mantener Fondo **Negro Puro**. La solidez del negro da seriedad a los precios.
6.  **GALLERY**: Mantener Fondo **Blanco**.
7.  **CTA FINAL**: Fondo **Blanco o Negro**.

---

## 2. Ajustes de Estilo por Sección (CSS/Inline)

### A. Sección Programs (Modalidades)
*   **Fondo:** Cambiar de oscuro a **Blanco (#FFFFFF)**.
*   **Cards:** Las tarjetas ya no deben ser "Dark Cards". Deben ser tarjetas blancas con borde Coral o una sombra sutil.

### B. Sección CTA Final
*   **Fondo:** Para cerrar con broche de oro, se recomienda que el CTA final use el fondo **Rosa Empolvado (#FFDCDC)** para que destaque sobre la galería blanca anterior y el footer negro posterior.

---

## 3. Instrucción Técnica de Movimiento de Bloques
1.  Cortar bloque `<!-- SPLIT — EL VALOR -->` (L158-L200 aprox).
2.  Pegar después de `<!-- HERO -->` y antes de `<!-- STATS BAR -->`.
3.  Asegurar que las líneas divisoras (`divider-line`) se mantengan entre cada bloque.

---
**Auditor:** Senior Technical Auditor
**Veredicto:** Este orden prioriza el "Storytelling" (Quiénes somos → Logros/Stats → Qué ofrecemos → Cuánto cuesta). Es mucho más vendedor.
