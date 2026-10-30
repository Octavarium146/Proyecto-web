# Jonas Sanche

Sitio web educativo sobre la música, trayectoria y presentaciones del rapero chileno Jonas Sanche. El proyecto reúne cinco páginas y aplica los contenidos estudiados durante el curso.

## Páginas

- **Inicio:** presentación, galería con carrusel y videoclip.
- **Sobre Jonas:** biografía, trayectoria y colaboraciones.
- **Música:** discografía con enlaces a plataformas musicales.
- **Detrás de la música:** documentales, entrevistas y conversaciones.
- **En vivo:** sesiones y presentaciones grabadas, con enlace a los anuncios oficiales.

## Tecnologías y recursos

- HTML5 semántico y responsive mobile-first.
- SCSS con variables, nesting, mixin con parámetros, `@extend` y partials.
- CSS compilado en `styles/style.css`.
- Flexbox, CSS Grid y breakpoints para tablet (768 px) y escritorio (1024 px).
- Bootstrap 5 por CDN: navbar en las cinco páginas, carrusel en Inicio y tarjetas en Música.
- Animación nativa con `@keyframes` y animaciones AOS en Música.
- Google Fonts: Permanent Marker y Kalam.
- Metadatos por página: título, descripción y keywords; imágenes con texto `alt`.

## Requisitos previos

Se necesita **Node.js** y **Sass** para trabajar con los estilos SCSS. Si Sass aún no está instalado, instala Node.js y ejecuta en una terminal:

```bash
npm install -g sass
```

## Estructura del proyecto

```text
proyecto/
├── index.html
├── pages/
│   ├── detras-de-la-musica.html
│   ├── en-vivo.html
│   ├── musica.html
│   └── sobre-mi.html
├── assets/                # Imágenes del sitio
├── scss/
│   ├── main.scss          # Punto de entrada con @use
│   ├── base/
│   ├── components/
│   ├── layout/
│   └── utilities/
├── styles/
│   └── style.css          # CSS compilado que usa el sitio
└── README.md
```

## Cómo abrir el sitio

Abre `index.html` en un navegador. Se necesita conexión a internet para cargar Bootstrap, Google Fonts, AOS y los contenidos externos.

## Dónde verificar los requisitos

- **Navbar y Bootstrap CDN:** en cada uno de los cinco HTML. El CSS de Bootstrap está en el `<head>` y el JavaScript antes de `</body>`.
- **Carrusel:** `index.html`, sección «Jonas Sanche en imágenes»; prueba las flechas para cambiar de imagen.
- **Tarjetas:** `pages/musica.html`, sección «Discografía».
- **Estados interactivos:** `:hover`, `:focus`, `:active` y `transition` en los enlaces de navegación, botones y elementos de la galería. Se prueban con el puntero, la tecla Tab y clic.
- **Animaciones:** animación nativa en `scss/base/_tipografia.scss`; AOS en `pages/musica.html`.
- **Responsividad:** reglas base mobile-first y media queries en `scss/layout/_responsive.scss`.
- **SCSS:** parciales en `scss/base/`, `scss/components/`, `scss/layout/` y `scss/utilities/`; `scss/main.scss` importa los parciales con `@use`.

## Repositorio y publicación

- **Repositorio público:** [GitHub](https://github.com/Octavarium146/Proyecto-web)
- **Sitio publicado en Netlify:** [proyectojonassanche.netlify.app](https://proyectojonassanche.netlify.app/)
- **Versión en GitHub Pages:** [octavarium146.github.io/Proyecto-web](https://octavarium146.github.io/Proyecto-web/)
