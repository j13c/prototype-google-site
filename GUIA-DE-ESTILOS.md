# Guía de estilos de Vortex

Esta guía define el lenguaje visual actual de la página y sirve como referencia para diseños nuevos. Mantén consistentes la paleta oscura, los acentos dorados, la tipografía y los componentes descritos aquí. La implementación actual está en `Vortex-rule.html`.

## Identidad visual

- **Tema:** oscuro, inspirado en una interfaz de juego.
- **Contraste:** superficies carbón y azul grisáceo con texto claro.
- **Acento:** dorado para acciones, iconos y contenido destacado.
- **Sensación:** compacta, legible y con brillos sutiles; evita sombras o decoraciones excesivas.

## Colores

Los valores principales corresponden a las variables CSS definidas en `:root`:

| Variable | Color | Uso |
|---|---|---|
| `--background` | `#323232` | Fondo principal de la página. |
| `--panel` | `#11161d` | Tono base oscuro de paneles. |
| `--panel-border` | `#242a33` | Bordes discretos de tarjetas. |
| `--text` | `#dedee1` | Texto general y contorno de enfoque. |
| — | `#f0eff0` | Títulos principales. |
| `--gold` | `#f5ca3d` | Acento, títulos secundarios, iconos, enlaces y texto destacado. |
| `--gold-border` | `#775c18` | Borde de etiquetas resaltadas. |
| `--gold-wash` | `rgba(245, 202, 61, 0.1)` | Fondo tenue de etiquetas. |
| — | `#b6b8bd` | Texto secundario, como pies de imagen. |
| — | `#15191e` | Detalles oscuros de los iconos de Pokébola. |

El fondo combina `--background` con un resplandor radial azul grisáceo tenue (`rgba(28, 35, 45, 0.34)`). Las tarjetas usan un degradado oscuro de `rgba(20, 25, 32, 0.97)` a `rgba(16, 21, 28, 0.97)`.

## Tipografía

- **Familia:** `Arial, Helvetica, sans-serif`.
- **Texto principal:** `--text`; peso normal de 500 y altura de línea compacta de 1.4 en las reglas.
- **Título principal:** color `#f0eff0`, peso 750, centrado y adaptable entre 42 y 76 px.
- **Títulos de sección:** color `--gold`, normalmente 20 px.
- **Texto de botón:** 15 px, peso 700; en móvil, 14 px.
- **Texto secundario:** 13 px.
- **Reglas:** escala entre 14 y 16 px en escritorio según el ancho disponible; 15 px en móvil, con altura de línea de 1.45.
- **Énfasis:** peso 700 y color `--gold`; usar etiquetas con fondo y borde tenues para términos importantes, no para párrafos completos.

## Componentes

### Botón de acción

- Forma de píldora (`border-radius: 999px`), borde dorado de 1 px y texto dorado.
- Fondo oscuro con degradado sutil y brillo dorado discreto.
- Icono SVG alineado junto al texto; tamaño aproximado de 22 px en escritorio y 20 px en móvil.
- En hover, elevar 1 px y aumentar ligeramente el brillo.
- Mantener foco de teclado visible: contorno claro de 3 px con separación de 5 px.

### Tarjetas y paneles

- Fondo oscuro en degradado, borde `--panel-border` de 1 px y esquinas redondeadas de 21 px.
- Sombra exterior suave; se permite un reflejo interior casi imperceptible.
- Usar el mismo tratamiento para nuevas secciones y tarjetas, evitando introducir colores de superficie distintos sin motivo.

### Pestañas

- Alinear la navegación de pestañas a la izquierda y el botón de registro a la derecha, en una misma fila cuando haya espacio.
- Usar botones compactos en forma de píldora, sin borde visible en reposo y con texto gris secundario.
- Mantener la tipografía de las pestañas igual a la del botón de registro: 15 px en escritorio y 14 px en móvil.
- La pestaña seleccionada lleva borde dorado oscuro, fondo dorado translúcido y texto dorado en negrita.
- Añadir estados hover y foco de teclado visibles; permitir navegar con flechas izquierda/derecha e Inicio/Fin.
- En pantallas estrechas, permitir que la navegación y el botón pasen a filas separadas sin desbordarse.
- Mantener bajo el espacio entre la fila superior y el panel para que las reglas quepan en la vista inicial.

### Lista de reglas

- Lista sin viñetas, dispuesta en cuadrícula.
- Cada fila combina icono, divisor vertical dorado y texto.
- Icono actual: Pokébola SVG de 28 px en dorado; sus detalles internos son oscuros.
- Divisor: dorado, de aproximadamente 3 × 27 px.
- Los términos destacados usan fondo dorado translúcido, borde oscuro dorado y esquinas redondeadas.

### Panel de entrenador

- En escritorio, presentar dos columnas: GIF a la izquierda y datos a la derecha.
- En móvil, apilar el GIF y los datos en una sola columna.
- Limitar el ancho del GIF a unos 260 px en escritorio y 210 px en móvil; usar contenedores de altura uniforme (320 px en escritorio y 260 px en móvil) para alinear los tres entrenadores.
- Presentar los campos como bloques oscuros con borde discreto; usar etiquetas gris secundario y valores claros.
- Mostrar el equipo Pokémon en etiquetas doradas dentro de una cuadrícula.
- Marcar claramente los datos provisionales como datos de ejemplo hasta que se sustituyan por los valores reales.

### Imágenes y sprites

- Mantener la proporción original (`height: auto`) y limitar el ancho al contenedor.
- Para pixel art, usar `image-rendering: pixelated` si se amplía.
- Centrar la imagen dentro de la tarjeta y usar pies de imagen en gris secundario.

### GIF de Tenor

- Los GIF de entrenadores se insertan mediante el embed oficial de Tenor en la columna izquierda del panel.
- El contenido visual y sus controles los proporciona Tenor; no asumir que el estilo interno del embed se puede personalizar desde la página.

## Espaciado y diseño adaptable

- El contenido se centra con un ancho máximo de 1030 px.
- En escritorio, el margen interior general es de 16 px arriba, 24 px a los lados y 20 px abajo.
- El punto de adaptación es `600px`.
- En móvil, reducir el margen exterior a 12 px, el relleno de tarjetas y el tamaño de iconos; conservar el orden y la alineación de los componentes.
- Mantener las reglas en 15 px en móvil para que sigan legibles; ajustar la altura de fila según el texto envuelto en varias líneas.
- Evitar anchos fijos para contenido que deba ajustarse a pantallas pequeñas.

## Guía para nuevas páginas y componentes

1. Reutiliza las variables CSS existentes antes de crear colores nuevos.
2. Usa el fondo de página y el tratamiento de tarjetas establecidos arriba.
3. Reserva el dorado para acciones, iconos y énfasis; no lo uses como color de párrafo largo.
4. Conserva la tipografía sans-serif y una jerarquía clara de títulos, texto y etiquetas.
5. Incluye estados hover y foco accesibles en elementos interactivos.
6. Para vistas agrupadas por tema, usa pestañas accesibles con un panel visible a la vez.
7. Diseña primero para el ancho disponible y verifica el punto de adaptación de 600 px.
8. Si la implementación cambia, actualiza esta guía para que siga describiendo los estilos reales.

## Referencia de implementación

La fuente actual de estilos es la sección `<style>` de `Vortex-rule.html`. Antes de modificar o crear componentes, consulta esta guía y reutiliza sus variables, proporciones y patrones cuando sea posible.
