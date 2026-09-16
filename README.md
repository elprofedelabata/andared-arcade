# Guía Andared_Corporativo

Guía interactiva para conectarse a **Andared_Corporativo**, la wifi de los centros educativos públicos de Andalucía.

👉 **https://elprofedelabata.github.io/guia-andared-corporativo/**

Pensada para repartir al claustro: eliges tu dispositivo y te lleva paso a paso, sin las 72 páginas de capturas del manual original.

## Estado

| Rama | Pantallas | Estado |
|---|---|---|
| **Ordenador** | Guadalinex EDU / EducaAndOS, Windows 7, Windows 8 y 8.1, Windows 10, Windows 11, Chrome OS | ✅ completa |
| Android | — | pendiente |
| Apple | — | pendiente |
| Otros (paneles del aula y gafas RV) | — | pendiente |

La rama Ordenador suma **58 pasos y 56 capturas**, con los dos procedimientos —conectar y olvidar la red— en cada una de sus seis pantallas.

## Cómo está hecho

Un único `index.html` sin dependencias ni proceso de compilación, más las capturas en `img/`. Se edita y se sube, nada más.

- **Estilo pixel retro**, sin degradados: colores planos, marcos de 4 px, sombras macizas y transiciones en `steps()`.
- **Iconos en SVG** dibujados como rectángulos sobre una rejilla de 16×16 con `shape-rendering="crispEdges"`, así que no hay ni una curva.
- **Tipografías** Press Start 2P y Silkscreen, servidas desde Google Fonts.
- **Transición en mosaico** entre pantallas: 12×8 celdas que entran en diagonal, dentro del interior y sin mover las barras.

### Estructura

Cada pantalla de procedimiento es una `<section class="pantalla larga">` con su `data-p`. La navegación la dispara cualquier elemento con `data-ir`, así que añadir una pantalla nueva es pegar la sección y enlazar su ficha, sin tocar el JavaScript.

### Las capturas

Salen del PDF oficial, optimizadas a WebP y con carga diferida. Un par de avisos para quien las toque:

- **Varias imágenes del PDF traen dos capturas dentro de un mismo archivo**, una al lado de otra. Hay que partirlas por el hueco blanco o los pasos acaban repitiendo la misma imagen.
- **El orden en que el PDF lista las imágenes no siempre es el orden en que están colocadas** en la página. Hay que ordenarlas por su posición, no por el listado.
- Antes de recortar nada, conviene **renderizar y mirar**: los recuadros rojos a veces están pintados semitransparentes sobre fondo oscuro y se pierden fácilmente.

## Publicación

GitHub Pages sirve la rama `main` desde la raíz. Cualquier cambio en `main` se publica solo en un par de minutos.

## Fuente

Adaptación de la *Guía de conexión de usuarios al servicio wifi corporativo de los centros educativos* (V13, 2 de junio de 2026), de la Agencia Pública Andaluza de Educación, Consejería de Desarrollo Educativo y Formación Profesional. El PDF original se publica junto a la guía.

Esto **no es un documento oficial**. Ante cualquier duda, manda la guía original de la Junta.
