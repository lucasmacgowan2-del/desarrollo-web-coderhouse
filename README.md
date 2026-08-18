# Portafolio Profesional de Desarrollo Web

**Proyecto Final Integrador** desarrollado por **Lucas Mac Gowan** para el curso de **Desarrollo Web** en **Coderhouse**.

---

## 🌐 Enlaces del Proyecto en Producción

* 🚀 **Sitio Web en Vivo (Producción / GitHub Pages)**:  
  [https://lucasmacgowan2-del.github.io/desarrollo-web-coderhouse/](https://lucasmacgowan2-del.github.io/desarrollo-web-coderhouse/)

* 📦 **Repositorio Público en GitHub**:  
  [https://github.com/lucasmacgowan2-del/desarrollo-web-coderhouse](https://github.com/lucasmacgowan2-del/desarrollo-web-coderhouse)

---

## 📁 Estructura del Proyecto

El proyecto sigue una arquitectura estricta y modular, separando la estructura HTML, los estilos SCSS, el CSS compilado y los activos multimedia:

```text
desarrollo-web-coderhouse/
├── index.html                  # Página principal de inicio (Home)
├── pages/                      # Páginas secundarias del sitio
│   ├── sobre-mi.html           # Información personal, valores y trayectoria
│   ├── proyectos.html          # Galería de proyectos y modales interactivos
│   ├── servicios.html          # Detalle de servicios y acordeón FAQ
│   └── contacto.html           # Formulario de contacto y datos de comunicación
├── scss/                       # Código fuente modular en SCSS
│   ├── main.scss               # Punto de entrada maestro (únicamente imports con @use)
│   ├── utilities/              # Tokens y herramientas globales
│   │   ├── _variables.scss     # Paleta de colores, tipografías, espaciados
│   │   └── _mixins.scss        # Mixins parametrizados y media queries
│   ├── base/                   # Reglas globales y tipografía
│   │   ├── _base.scss          # Reset universal del Box Model y body
│   │   └── _typography.scss    # Jerarquía tipográfica con clamp() y rem
│   ├── layout/                 # Estructura general de las páginas
│   │   ├── _header.scss        # Estilos del encabezado
│   │   ├── _nav.scss           # Navegación y enlaces
│   │   └── _footer.scss        # Pie de página y enlaces sociales
│   └── components/             # Componentes reutilizables
│       ├── _buttons.scss       # Estilos y estados de botones
│       ├── _cards.scss         # Tarjetas con @extend y @keyframes nativos
│       └── _grid.scss          # Grillas bidimensionales responsivas
├── styles/
│   └── styles.css              # Hoja de estilos final compilada desde SCSS
├── assets/
│   └── images/                 # Fotografías y recursos visuales optimizados
│       ├── perfil.jpg
│       ├── escritorio-trabajo.jpg
│       ├── proyectos-galeria.jpg
│       ├── servicios-web.jpg
│       └── contacto-oficina.jpg
├── .gitignore                  # Exclusión de temporales y dependencias
└── README.md                   # Documentación completa del proyecto
```

---

## 🛠️ Tecnologías y Criterios Técnicos Implementados

1. **HTML5 Semántico y Accesibilidad**:
   * Uso estricto de etiquetas semánticas (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<figure>`, `<figcaption>`).
   * Jerarquía de encabezados ordenada sin saltos (`<h1>` → `<h2>` → `<h3>`).
   * Atributos `alt` descriptivos y detallados en todas las imágenes.

2. **Arquitectura SCSS Modular**:
   * Estructura basada en partials (`_*.scss`) organizados por carpetas (`utilities`, `base`, `layout`, `components`).
   * Uso exclusivo de `@use` en `main.scss` como único punto de entrada.
   * Implementación de variables `$`, anidamiento (*nesting* hasta 3 niveles), selector ampersand `&`, `@mixin` con parámetros, `@include` y herencia con `%placeholder` + `@extend`.

3. **Diseño Responsivo y Mobile-First**:
   * Enfoque *Mobile-First* garantizando adaptabilidad en celulares, tablets (`min-width: 768px`) y escritorio (`min-width: 1024px`).
   * Combinación de **CSS Grid** (2D) para el layout maestro y **Flexbox** (1D) para la alineación interna de componentes.
   * Tipografía fluida y escalable mediante `clamp()` y unidades relativas `rem`.

4. **Bootstrap 5.3**:
   * Integración de Bootstrap 5.3 CDN para el Navbar responsivo con menú hamburguesa colapsable en pantallas pequeñas.
   * Componentes interactivos: Carousel en la portada, Acordeón de preguntas frecuentes / habilidades y Ventanas Modales (`data-bs-toggle="modal"`).
   * Estilado personalizado de componentes desde SCSS para mantener la identidad visual del diseño.

5. **Animaciones y Efectos Visuales**:
   * **Animaciones Nativas**: Transiciones suaves en estados `:hover`/`:active` y animación `@keyframes floatHero` en CSS/SCSS.
   * **Librería Externa**: Integración de **AOS (Animate On Scroll)** mediante CDN para animaciones de entrada fluidas (`fade-up`, `zoom-in`).

6. **SEO On-Page**:
   * Etiquetas `<title>`, `<meta name="description">` y `<meta name="keywords">` únicas y representativas en cada uno de los 5 archivos HTML.
   * Nombres de archivos descriptivos y URLs amigables.

---

## 💻 Compilación de Estilos

Para compilar los estilos de SCSS a CSS en modo observador:

```bash
npx sass --watch scss/main.scss styles/styles.css --no-source-map
```
