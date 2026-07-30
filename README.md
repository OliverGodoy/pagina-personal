# Página Personal 
# - Oliver Isaac Godoy Salguero

Sitio web de presentación personal / currículum digital, desarrollado con HTML5 semántico y Bootstrap 5, aplicando diseño responsive y personalización visual propia mediante CSS.

##  Objetivo del proyecto

Este proyecto tiene como propósito aprender a integrar un framework CSS moderno (Bootstrap 5) sin perder identidad visual propia. El sitio funciona como perfil/portafolio digital, mostrando información personal, habilidades, proyectos destacados y visión profesional, cumpliendo con principios de HTML5 semántico, diseño responsive y accesibilidad básica.

##  Cómo ejecutar la página

No requiere instalación ni dependencias locales, ya que Bootstrap se consume vía CDN.

1. Clona o descarga este repositorio.
2. Abre el archivo `index.html` directamente en tu navegador (doble clic, o clic derecho → "Abrir con" tu navegador preferido).

No es necesario un servidor local, aunque también puedes usar una extensión como *Live Server* (VS Code) si prefieres recarga automática al editar.

##  Componentes de Bootstrap utilizados

- **Navbar** (`navbar`, `navbar-expand-lg`, `navbar-toggler`, `navbar-collapse`): barra de navegación responsive, colapsable en pantallas menores a 992px, con atributos de accesibilidad (`aria-expanded`, `aria-controls`, `aria-label`).
- **Grid system** (`container`, `row`, `col-md-*`, `col-lg-*`): utilizado en el hero (imagen + texto en columnas), en la sección de proyectos (3 cards responsivas) y en el footer.
- **Cards** (`card`, `card-img-top`, `card-body`, `card-title`, `card-text`): utilizadas para mostrar los 3 proyectos destacados, cada una con imagen, título, descripción y botón de enlace a GitHub.
- **Badges / Rounded pills** (`badge`, `rounded-pill`): utilizados en la sección de Habilidades para mostrar las 5 tecnologías/herramientas de forma compacta.
- **Botones** (`btn`, `btn-primary`): utilizados en las cards de proyectos.
- **Utilidades de Flexbox** (`d-flex`, `flex-wrap`, `flex-column`, `align-items-center`, `gap-2`, `mt-auto`, `align-self-start`): utilizadas para alinear badges, centrar el hero verticalmente y anclar los botones de las cards al final del contenedor sin depender del largo del texto.
- **Utilidades responsive de texto** (`text-center`, `text-md-start`): para centrar contenido en móvil y alinearlo a la izquierda en pantallas más grandes.
- **Utilidades de espaciado** (`py-3`): para dar espaciado vertical consistente entre secciones.

##  Elementos personalizados mediante CSS

Todo el archivo `css/style.css` se encarga de aportar identidad visual propia sobre la base de Bootstrap, sin usar `!important` en ningún momento (las sobrescrituras se logran redefiniendo las variables CSS internas de Bootstrap, como `--bs-primary` y las variables locales de `.btn-primary`).

- **Colores**: paleta propia en tono verde/teal, definida mediante variables CSS (`--color-primario`, `--color-primario-claro`, `--color-secundario`, `--color-fondo-suave`), aplicada a badges, botones, navbar (marca y enlaces con hover) y footer.
- **Tipografía**: fuente **Inter** (Google Fonts), reemplazando la fuente por defecto del sistema. Se ajustó `font-weight` y `letter-spacing` en los encabezados para reforzar la jerarquía visual.
- **Espaciados**: uso de la utilidad `py-3` de Bootstrap en todas las secciones principales para mantener separación consistente.
- **Sombras**: `box-shadow` sutil en las cards de proyectos, reemplazando el borde plano por defecto de Bootstrap.
- **Animaciones/transiciones**:
  - Efecto de elevación (`transform: translateY`) y sombra más marcada al pasar el mouse sobre una card de proyecto.
  - Transición de color en los enlaces del navbar y del footer al pasar el mouse.
- **Ajuste de imágenes en cards**: `object-fit: contain` con altura fija en `.card-img-top`, para que las imágenes de los 3 proyectos (de proporciones distintas) se muestren de forma consistente sin deformarse ni recortarse.

##  Principales decisiones de diseño

- **Estructura semántica primero, estilos después**: el proyecto se construyó por etapas — primero el HTML5 semántico puro, luego la integración de Bootstrap componente por componente, y al final la personalización visual. Esto se refleja en el historial de commits del repositorio.
- **Mobile-first**: todas las columnas del grid se definieron pensando primero en el comportamiento por defecto (apilado en móvil) y luego añadiendo comportamiento específico para pantallas más grandes (`col-md-*`, `col-lg-*`), siguiendo el enfoque nativo de Bootstrap.
- **Layout de proyectos**: se decidió mostrar las 3 cards en una sola fila en pantallas grandes (`col-lg-4`), 2 por fila en tablet (`col-md-6`) y apiladas en móvil, priorizando que las 3 tarjetas se vean equilibradas en desktop.
- **Personalización sin romper Bootstrap**: en vez de sobrescribir clases con alta especificidad o `!important`, se optó por redefinir las variables CSS que Bootstrap 5 expone internamente, tanto a nivel global (`--bs-primary`) como a nivel de componente (variables locales de `.btn-primary`), manteniendo el código limpio y mantenible.
- **Navbar minimalista**: se eligió un navbar de fondo claro con acentos en verde (en vez de un navbar de fondo oscuro), para transmitir un estilo sobrio y profesional acorde a un portafolio de desarrollador.
- **Accesibilidad como criterio transversal**: atributos `alt` descriptivos, atributos ARIA en el botón del navbar, uso de `rel="noopener noreferrer"` en enlaces externos, y jerarquía de encabezados (`h1` → `h2` → `h3`) respetada en todas las secciones.

##  Responsive

El sitio fue verificado manualmente en los siguientes anchos, sin generar desplazamiento horizontal:

| Ancho | Comportamiento |
|---|---|
| 320px | Navbar colapsado (menú hamburguesa), contenido apilado en una sola columna |
| 768px | Navbar aún colapsado (breakpoint de expansión es `lg`, 992px), cards de proyectos en 2 columnas |
| 1280px | Navbar expandido con los 4 enlaces visibles, cards de proyectos en una sola fila de 3 |

Capturas de pantalla de estos 3 tamaños se incluyen en la carpeta `/screenshots` del repositorio.

## 📂 Estructura del proyecto

```
/
├── index.html
├── css/
│   └── style.css
├── imgs/
│   ├── profile.jpg
│   ├── proyecto1.png
│   ├── proyecto2.png
│   └── proyecto3.png
├── screenshots/
│   ├── 320px.png
│   ├── 768px.png
│   └── 1280px.png
└── README.md
```

## 👤 Autor

**Oliver Isaac Godoy Salguero**
- GitHub: [OliverGodoy](https://github.com/OliverGodoy)
- LinkedIn: [oliver-godoy](https://www.linkedin.com/in/oliver-godoy-282817416/)
- Correo: ogodoys@miumg.edu.gt