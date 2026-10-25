# Jonas Sanche

Proyecto educativo de un sitio web dedicado a la música y trayectoria de Jonas Sanche.

## Páginas

- **Inicio:** presentación del artista, galería, videoclip y contacto profesional.
- **Sobre Jonas:** biografía, trayectoria y colaboraciones.
- **Música:** discografía con enlaces a Spotify y Apple Music.
- **Detrás de la música:** documental, entrevistas y podcast.
- **En vivo:** agenda de presentaciones y actuaciones grabadas.

## Tecnologías

- HTML5, SCSS y CSS compilado.
- Flexbox y CSS Grid.
- Bootstrap mediante CDN.
- Google Fonts: Permanent Marker y Kalam.

## Requisitos previos

Se necesita **Node.js** para utilizar npm y **Sass** para compilar los estilos SCSS. Si Sass aún no está instalado, abre una terminal y ejecuta:

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
├── img/                   # Imágenes del sitio
├── scss/
│   ├── main.scss          # Punto de entrada SCSS
│   ├── base/
│   ├── components/
│   ├── layout/
│   └── utilities/
├── styles/
│   └── style.css          # CSS compilado que usa el sitio
└── README.md
```

## Sitio web

[Ver sitio publicado](https://octavarium146.github.io/Proyecto-web/)

## Bootstrap y estados interactivos

### Dónde revisar

- **Navbar de Bootstrap:** está en `index.html`, `pages/sobre-mi.html`, `pages/musica.html`, `pages/detras-de-la-musica.html` y `pages/en-vivo.html`. En cada uno, Bootstrap CSS 5.3.8 está vinculado dentro de `<head>` antes de `styles/style.css` y el archivo `bootstrap.bundle.min.js` está antes de `</body>`. La clase `navbar-expand-lg` y el botón `navbar-toggler` permiten comprobar el menú responsivo.
- **Carrusel de Bootstrap:** está en `index.html`, en la sección «Jonas Sanche en imágenes», con el identificador `galeria-jonas` y sus controles anterior y siguiente.
- **Tarjetas de Bootstrap:** están en `pages/musica.html`, en la sección «Discografía», con las clases `card`, `card-img-top`, `card-title` y `card-text`.
- **Clases propias que adaptan Bootstrap a la paleta del sitio:** `barra-principal`, `enlace`, `boton`, `control`, `galeria` y `tarjeta`. Sus estilos están en `scss/layout/_nav.scss`, `scss/components/_buttons.scss`, `scss/components/_galeria.scss` y `scss/components/_cards.scss`. El archivo `styles/style.css` contiene los estilos compilados que carga el HTML.

### Cómo comprobar los criterios

1. **Bootstrap en las cinco páginas:** revisa los enlaces CDN de CSS y JavaScript en los archivos HTML indicados arriba. El CSS de Bootstrap precede a la hoja propia.
2. **Navbar responsiva:** abre una página en una ventana estrecha y comprueba que aparezca el botón de menú; presiónalo para mostrar y ocultar los enlaces. En una ventana ancha, los enlaces se muestran expandidos.
3. **Componentes:** en Inicio, usa las flechas del carrusel para cambiar de imagen. En Música, revisa las tarjetas de discografía y sus botones.
4. **Pseudoclases y transiciones:** en `scss/layout/_nav.scss` se encuentran `:hover`, `:focus` y `:active` para los enlaces. En `scss/components/_buttons.scss` están los estados de botones y controles; en `scss/components/_galeria.scss`, los de la galería; y en `scss/components/_cards.scss`, el estado `:hover` de las tarjetas.
5. **Prueba interactiva:** pasa el puntero sobre enlaces, botones y tarjetas; usa `Tab` para llegar a los elementos y comprobar el estado de foco; y haz clic para observar el estado activo. Los cambios visuales usan `transition` en los estilos SCSS correspondientes, compartidos por las páginas.
