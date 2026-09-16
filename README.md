# Andared Arcade

Guía interactiva para conectarse a **Andared_Corporativo**, la wifi de los centros educativos públicos de Andalucía.

👉 **https://elprofedelabata.github.io/andared-arcade/**

Pensada para repartir al claustro: eliges tu dispositivo y te lleva paso a paso, sin las 72 páginas de capturas del manual original.

## Qué cubre

| Rama | Pantallas |
|---|---|
| **Ordenador** | Guadalinex EDU / EducaAndOS · Windows 7 · Windows 8 y 8.1 · Windows 10 · Windows 11 · Chrome OS |
| **Android** | móvil o tablet |
| **Apple** | iPhone, iPad y Mac |
| **Otros** | DDA Vexia · Gafas RV *(Meta Quest, HTC Vive, DPVR E4)* · Panel Smart · Panel Newline · Panel ViewSonic |

Trece pantallas de procedimiento, **128 pasos y 107 capturas**, con conectar y olvidar la red en cada una. Las gafas RV son la excepción: el manual original no trae apartado de olvidar red para ellas, así que esa pantalla usa las pestañas para elegir modelo.

## Cómo está hecho

Un único `index.html` sin dependencias ni proceso de compilación, más las capturas en `img/` y dos audios. Se edita y se sube, nada más.

- **Estilo pixel retro**, sin degradados: colores planos, marcos de 4 px, sombras macizas y transiciones en `steps()`.
- **Iconos en SVG** dibujados como rectángulos sobre una rejilla de 16×16 con `shape-rendering="crispEdges"`, así que no hay ni una curva.
- **Transición en mosaico** entre pantallas: 12×8 celdas que entran en diagonal, dentro del interior y sin mover las barras.

### Los cuatro mandos del pie

Tema claro u oscuro, sonido de clic, música de fondo y tipo de letra. Los cuatro recuerdan la elección en el navegador.

- El **modo claro** no es el oscuro invertido: conserva el sesgo índigo del fondo y oscurece los colores de rama hasta que se leen sobre blanco.
- El **modo legible** cambia a [Atkinson Hyperlegible](https://www.brailleinstitute.org/freefont/), del Braille Institute, que separa la I mayúscula de la l minúscula y del 1, y la O del cero. Importa: media guía son cosas que hay que teclear sin equivocarse.
- Los **audios se descargan solo si los activas**. La música son 4,4 MB.

### Estructura

Cada pantalla de procedimiento es una `<section class="pantalla larga">` con su `data-p`. La navegación la dispara cualquier elemento con `data-ir`, así que añadir una pantalla nueva es pegar la sección y enlazar su ficha, sin tocar el JavaScript.

### Las capturas

Salen del PDF oficial, optimizadas a WebP y con carga diferida. Tres avisos para quien las toque:

- **Varias imágenes del PDF traen dos o tres capturas dentro de un mismo archivo**, una al lado de otra. Hay que partirlas por el hueco blanco o los pasos acaban repitiendo la misma imagen.
- **El orden en que el PDF lista las imágenes no siempre es el orden en que están colocadas** en la página. Hay que ordenarlas por su posición, no por el listado.
- Antes de recortar nada, conviene **renderizar y mirar**: los recuadros rojos a veces están pintados semitransparentes sobre fondo oscuro y se pierden fácilmente.

## Publicación

GitHub Pages sirve la rama `main` desde la raíz. Cualquier cambio en `main` se publica solo en un par de minutos.

## Fuente

Adaptación de la *Guía de conexión de usuarios al servicio wifi corporativo de los centros educativos* (V13, 2 de junio de 2026), de la Agencia Pública Andaluza de Educación, Consejería de Desarrollo Educativo y Formación Profesional. El PDF original se publica junto a la guía.

Esto **no es un documento oficial**. Ante cualquier duda, manda la guía original de la Junta.
