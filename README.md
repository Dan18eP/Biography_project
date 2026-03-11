# Biography Project

# 🐐 Lionel Messi: Un 10 de Historia — Página Biográfica

Proyecto de desarrollo web estático dedicado a la biografía de Lionel Messi. Construido con HTML5, Bootstrap 5.2 y CSS personalizado.

---

## Estructura del proyecto

```
proyecto-messi/
├── index.html
├── favicon.ico
├── css/
│   └── styles.css
├── js/
│   └── script.js
└── img/
    ├── messigif.gif
    ├── LeoFCB.jpg
    ├── msn2.jpg
    ├── messi1.jpg
    ├── messi2.jpg
    ├── messi3.jpg
    └── msn.jpg
```

---

## Tecnologías utilizadas

| Tecnología | Versión | Uso |
|---|---|---|
| HTML5 | — | Estructura semántica de la página |
| Bootstrap | 5.2.3 | Layout responsivo, componentes y utilidades |
| CSS personalizado | — | Estilos visuales propios y animaciones |
| Google Fonts (Poppins) | — | Tipografía principal |

---

## Estructura del HTML

La página está compuesta por las siguientes secciones, navegables mediante el menú de navegación fijo:

### `<nav>` — Barra de navegación
- Barra fija en la parte superior (`fixed-top`) con color oscuro.
- Incluye el nombre del sitio como `navbar-brand` y enlaces de navegación internos con anclas (`#inicio`, `#biografia`, etc.).
- Colapsa en pantallas pequeñas usando el toggler de Bootstrap.
- Activa **scroll spy** de Bootstrap (`data-bs-spy="scroll"`) para resaltar la sección activa mientras se navega.

### `#inicio` — Hero / Portada
- Sección principal con fondo degradado y texto centrado.
- Incluye un GIF animado de Messi con la Copa del Mundo dentro de un `<img>` circular con la clase `.imagen-messi`.
- Contiene una tarjeta (`card`) con descripción introductoria del jugador.

### `#biografia` — Biografía
- Layout de dos columnas con Bootstrap (`col-md-6`).
- Columna izquierda: texto biográfico y línea de tiempo vertical (`.timeline`) con eventos clave de la carrera de Messi.
- Columna derecha: dos fotografías del jugador con pie de foto.

### `#logros` — Logros
- Cuatro tarjetas (`col-md-3`) con información sobre:
  - Champions League
  - Títulos con la Selección Argentina
  - Estadísticas por club
  - Balones de Oro

### `#galeria` — Galería
- Cuatro imágenes en grilla responsiva (`col-12 col-sm-6 col-md-3`).
- Cada imagen tiene un pie de foto descriptivo y efecto hover.

### `#contacto` — Contacto
- Formulario con campos de nombre, correo electrónico y mensaje.
- Botón de envío con estilo primario de Bootstrap.

### `<footer>` — Pie de página
- Fondo oscuro con texto blanco centrado.
- Incluye créditos del autor y año.

---

## Estilos CSS (`styles.css`)

### Cuerpo y tipografía
- **Fuente principal:** `Poppins` (importada desde Google Fonts).
- **Fondo del body:** degradado diagonal (`linear-gradient`) en tonos azul claro y gris, que cubre toda la altura de la ventana (`min-height: 100vh`).
- **Párrafos:** `line-height: 1.7`, color gris oscuro `#444` y tamaño `1.05rem` para mejor legibilidad.

### Sección Hero (`#inicio` y `.hero`)
- `#inicio`: fondo semitransparente con `linear-gradient`.
- `.hero`: color principal azul `#00aae7`, padding generoso (`120px 0`).
- `.hero::after`: pseudo-elemento decorativo que simula una ola en la parte inferior de la sección usando `border-radius: 50% 50% 0 0`.

### Imágenes (`.imagen-messi`)
- Borde blanco de 3px y sombra difuminada.
- Efecto de escala al hacer hover con transición suave (`transform: scale(1.02)` en `0.3s`).

### Encabezados
- `h1`: negrita y margen inferior.
- `h2`: centrado, negrita, y un subrayado decorativo generado con `::after` (línea azul de 70px de ancho).

### Tarjetas (`.card`)
- Sin borde visible, bordes redondeados (`border-radius: 12px`) y sombra suave.
- Efecto de elevación al hacer hover: `translateY(-10px)` con transición de `0.2s`.

### Galería (`.gallery-img`)
- Tamaño fijo de `600x400px` con `object-fit: cover` para recorte uniforme.
- Al hacer hover: escala ligeramente y agrega sombra pronunciada.

### Línea de tiempo (`.timeline`)
- Borde izquierdo azul de 3px como línea vertical.
- `.timeline-year`: año en negrita y color azul primario.

### Navbar
- Sombra inferior sutil en la barra de navegación.
- Enlace activo resaltado en azul `#00aae7` con `font-weight: 600`.
- Transición de color en los enlaces al hacer hover.

### Divisor de secciones (`.section-divider`)
- Línea decorativa de 60px de ancho, 3px de alto y color azul, centrada entre secciones.

### Secciones generales (`section`)
- `padding-top/bottom: 70px` uniforme.
- `scroll-margin-top: 150px` para que el scroll spy compense la altura del navbar fijo.

---

## Buenas prácticas aplicadas

- Uso de atributos `alt` descriptivos en todas las imágenes para accesibilidad.
- Jerarquía semántica de encabezados (`h1` → `h2` → `h4`, `h5`, `h6`).
- Diseño responsivo con el sistema de grillas de Bootstrap.
- Navegación con anclas internas y scroll spy para mejorar la experiencia de usuario.
- Separación de responsabilidades: estructura en HTML, estilos en CSS externo.

---

## Autor

**Daniel Echeverría** — Proyecto Desarrollo Web, 2026