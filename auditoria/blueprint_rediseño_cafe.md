# Blueprint de Rediseño: Me Gusta Café (v2)
**Estado:** 🔴 REQUIERE IMPLEMENTACIÓN COMPLETA
**Objetivo:** Transformar `cafe.html` en una galería de café de especialidad, eliminando marrones "enlodados" y aplicando la tríada de lujo: **Blanco / Negro / Rosa** + **Verde de Marca**.

## 1. Cambios Globales (CSS & Head)
*   **Background:** Cambiar `body { background: #fdf6ec }` por `background: #ffffff`.
*   **Paleta:** Sustituir todo rastro de `#8b4513` (marrón) por `#000000` (Negro) o `#5aaa6a` (Verde).

---

## 2. Sección por Sección (Estructura & Estilo)

### A. Hero Cinematográfico
*   **Título:** Eliminar itálicas y forzar mayúsculas.
*   **Código:**
    ```html
    <h1 class="serif" style="font-size:clamp(3rem,6vw,5.2rem); text-transform:uppercase; color:#fff">
      Me Gusta <span style="color:#5aaa6a">CAFÉ</span>
    </h1>
    ```

### B. Info Bar (Ubicación y Horas)
*   **Fondo:** Negro Puro (`#000000`).
*   **Iconos:** Verde (`#5aaa6a`).
*   **Texto:** Blanco con opacidad 0.8.

### C. Intro & Carrusel (White Section)
*   **Fondo:** Blanco Puro (`#FFFFFF`).
*   **Cápsulas de Texto:** Cambiar el fondo beige `#f3e8dc` por un **Rosa Empolvado suave** (`rgba(255,220,220,0.3)`) o Blanco con borde Negro.
*   **Bordes:** Asegurar que el carrusel tenga `border-radius: 0`.

### D. Sección "Dos Orígenes" (Dark Section)
*   **Fondo:** Negro Puro (`#000000`).
*   **Cards:** Fondo `#111111` (Gris casi negro).
*   **Acento Lavazza:** Usar **Rojo Marca (#D61A16)** para conectar con la marca madre.
*   **Acento Jaqaku:** Usar **Verde Marca (#5aaa6a)**.

---

## 3. El Nuevo CTA Editorial (Cierre de Página)
Sustituir el bloque actual por este diseño de alta gama:

```html
<!-- CTA EDITORIAL - CAFÉ -->
<section class="cafe-cta-editorial" style="background:#ffffff; padding:140px 24px; position:relative; overflow:hidden">
  
  <!-- "CAFE" en Aztec Beat gigante de fondo -->
  <div style="position:absolute; top:50%; left:50%; transform:translate(-50%,-50%); font-family:'Aztec Beat'; font-size:35vw; color:#FFDCDC; opacity:0.12; pointer-events:none; z-index:0; letter-spacing:-10px">
    CAFE
  </div>

  <div style="position:relative; z-index:1; max-width:800px; margin:0 auto; text-align:center">
    <p class="eyebrow" style="color:#5aaa6a; margin-bottom:32px">Bolivar 603 · Sucre</p>
    
    <h2 style="font-family:'Aztec Beat',serif; font-size:clamp(2.5rem, 6vw, 4.2rem); text-transform:uppercase; color:#000000; line-height:1; margin-bottom:40px">
      Where the morning <br> 
      <span style="color:#5aaa6a">takes its time.</span>
    </h2>

    <p style="font-family:'Inter',sans-serif; font-size:18px; color:#555; line-height:1.8; max-width:540px; margin:0 auto 56px">
      Bolivian coffee at altitude, food made from scratch, and a colonial patio where Sucre slows down.
    </p>

    <div class="flex flex-wrap justify-center" style="gap:24px">
      <a href="https://www.megustaspanish.com/cafe" target="_blank" class="btn-black" style="padding:18px 48px">Visit our Website ↗</a>
      <a href="https://maps.google.com/?q=Bolivar+603+Sucre+Bolivia" target="_blank" style="font-family:'Inter'; font-weight:700; text-transform:uppercase; font-size:12px; letter-spacing:2px; color:#000; text-decoration:none; display:flex; align-items:center; gap:8px">
        Find us on Maps
      </a>
    </div>
  </div>
</section>
```

---
**Auditor:** Senior Technical Auditor
**Veredicto:** Este rediseño unifica el Café con la nueva identidad visual de Me Gusta Sucre, elevando la percepción de calidad de "cafetería común" a "experiencia de especialidad".
