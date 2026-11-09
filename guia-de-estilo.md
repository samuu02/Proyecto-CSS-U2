# La Partida · Guía de estilo

Microproyecto de la UD 2 (A02.4 a A02.9). La Partida es una tienda y ludoteca de juegos de mesa de
barrio inventada. Tienes que maquetar sus dos páginas, `index.html` y `torneos.html`, para que
coincidan con el diseño de la carpeta `diseno/`. El HTML ya está escrito y tiene todas las clases:
no lo cambies, salvo para añadir los `<link>` de tus hojas y el `srcset` de la imagen de la portada.

## Diseño

| Captura                                                    | Qué muestra                                      |
| ---------------------------------------------------------- | ------------------------------------------------ |
| `inicio-movil.png`, `torneos-movil.png`                    | Las dos páginas a 390 px de ancho                |
| `inicio-escritorio.png`, `torneos-escritorio.png`          | Las dos páginas a 1440 px de ancho               |
| `inicio-escritorio-oscuro.png`, `torneos-movil-oscuro.png` | El tema oscuro                                   |
| `inicio-impresion.png`, `torneos-impresion.png`            | La primera hoja de cada página al imprimir en A4 |

Entre 390 y 1440 px, el diseño se adapta solo: no hay más capturas.

## Colores

| Nombre               | Tema claro  | Tema oscuro | Uso                                                                                                                    |
| -------------------- | ----------- | ----------- | ---------------------------------------------------------------------------------------------------------------------- |
| Primario             | `#5B2A86`   | igual       | Botones, enlaces, cifras, fecha de los eventos                                                                         |
| Primario oscuro      | `#40205F`   | igual       | Botón al pasar el ratón, cabecera de la tabla, pie                                                                     |
| Acento               | `#F2C14E`   | igual       | Etiquetas, números de las cifras, borde del precio destacado. **Nunca como color de texto sobre fondo claro** (1,54:1) |
| Fondo                | `#F7F4FB`   | `#15111B`   | Fondo de la página y filas pares de la tabla                                                                           |
| Superficie           | `#FFFFFF`   | `#211A2A`   | Cabecera, portada, tarjetas, precios, tabla                                                                            |
| Texto                | `#241B2F`   | `#EEE9F4`   | Texto general                                                                                                          |
| Texto suave          | `#5F566B`   | `#B8AEC6`   | Antetítulo, datos de los eventos, unidades de los precios, notas                                                       |
| Borde suave          | `#DCD5E5`   | `#3B3247`   | Líneas de la tabla y de los eventos, borde de los precios, etiqueta «Completo»                                         |
| Enlace               | el primario | `#CBA6F0`   | Enlaces, iconos, importes, botones de contorno                                                                         |
| Texto sobre primario | `#FFFFFF`   | igual       | Sobre el primario y el primario oscuro                                                                                 |
| Texto sobre acento   | `#241B2F`   | igual       | Sobre el acento                                                                                                        |

Contrastes (WCAG): texto sobre fondo, 15,15:1; texto suave sobre superficie, 6,93:1; enlace sobre
fondo, 9,10:1; blanco sobre primario, 9,90:1; acento sobre primario, 5,90:1. En el tema oscuro:
texto sobre superficie, 14,12:1; texto suave, 7,95:1; enlace, 8,23:1. Todos cumplen AA.

En el tema oscuro, la sombra desaparece. Los colores de la marca no cambian.

## Tipografía

Las dos familias se cargan desde Google Fonts con el `<link>` que ya está en el HTML (licencia SIL
Open Font License). Termina siempre la lista con la familia genérica `sans-serif`.

| Uso                                                     | Familia | Peso                                                   |
| ------------------------------------------------------- | ------- | ------------------------------------------------------ |
| Títulos, logotipo, cifras, día de los eventos, importes | Fredoka | 600                                                    |
| Texto                                                   | Nunito  | 400 y 700 (negrita: enlaces, botones, menú, etiquetas) |

Escala: el texto base mide 16 px con interlineado 1,5; los títulos, 1,2 (los de la portada y los
importes, 1,1). Los títulos crecen **de forma continua** entre los dos anchos del diseño:

| Elemento                                     | A 390 px o menos | A 1440 px o más |
| -------------------------------------------- | ---------------- | --------------- |
| Título de la portada y números de las cifras | 40 px            | 56 px           |
| `h1` e importes de los precios               | 32 px            | 44 px           |
| `h2`                                         | 26 px            | 32 px           |
| `h3`                                         | 20 px            | 24 px           |
| Entradilla                                   | 20 px            | 20 px           |
| Texto pequeño (etiquetas)                    | 14 px            | 14 px           |

## Espacios, retícula y formas

- **Espaciado:** múltiplos de 4 px: 4, 8, 16, 24, 32, 48 y 64.
- **Retícula del móvil:** una columna, márgenes laterales de 16 px y medianil de 16 px.
- **Retícula de escritorio, a partir de 768 px:** 12 columnas, ancho máximo del contenido de
  1120 px, centrado; márgenes laterales y medianil de 24 px.
- **Secciones:** 48 px de relleno arriba y abajo.
- **Esquinas:** botones totalmente redondeados; tarjetas, precios, imagen y fecha de los eventos,
  12 px; etiquetas, 4 px.
- **Sombra:** `0 2px 8px` con el color del texto al 12 % de opacidad.

## Componentes

| Componente | Cómo es                                                                                                                                                                                                                                                                                |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Botón      | Relleno de 12 px arriba y abajo y 24 px a los lados; borde de 2 px; negrita. Principal: fondo primario y texto blanco; al pasar el ratón, primario oscuro. **De contorno**: fondo transparente, y el borde y el texto del color de los enlaces; al pasar el ratón, fondo de superficie |
| Etiqueta   | Relleno de 4 px y 8 px; 14 px en negrita; fondo acento. **«Completo»**: fondo borde suave y color de texto. **En la esquina**: a 16 px de los bordes superior y derecho de su tarjeta; en el precio destacado, centrada sobre el borde superior                                        |
| Tarjeta    | Relleno de 24 px, superficie y sombra. Icono de 48 px del color de los enlaces, con 16 px debajo                                                                                                                                                                                       |
| Logotipo   | Icono de 32 px y el nombre en Fredoka de 24 px, separados 8 px, del color de los enlaces (blanco en el pie)                                                                                                                                                                            |
| Menú       | Enlaces en negrita del color del texto, sin subrayar. Página actual y al pasar el ratón: color de los enlaces y subrayado de 3 px separado 6 px del texto                                                                                                                              |
| Evento     | La fecha en una caja de 72 px de ancho, a la izquierda, con relleno de 8 px, fondo primario, texto blanco en mayúsculas y el día en Fredoka de 28 px; a su lado, el título y los datos (texto suave), centrados en vertical. 16 px entre la fecha y el texto; línea inferior de 1 px   |
| Cifra      | El número en Fredoka, del tamaño del título de la portada y de color acento; debajo, el texto. Centrada                                                                                                                                                                                |
| Precio     | Relleno de 24 px, borde de 2 px del color borde suave, superficie. Importe en Fredoka del tamaño del `h1`; la unidad, en 16 px y texto suave. Viñetas del color de los enlaces. El botón, siempre al final de la tarjeta. **Destacado**: borde acento y sombra                         |
| Tabla      | Todo el ancho, 640 px como mínimo. Celdas con relleno de 12 px y 16 px y línea inferior; cabecera en primario oscuro con texto blanco; filas pares con el color de fondo; números alineados a la derecha; título (`caption`) en negrita a la izquierda                                 |
| Foco       | Contorno de 2 px del color del texto, separado 2 px (en el pie, blanco)                                                                                                                                                                                                                |

## Disposición

| Zona              | Móvil                                                                                                           | Escritorio (desde 768 px)                                                                                                            |
| ----------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Cabecera          | Logotipo y, debajo, el menú. Se queda fija arriba al desplazar la página                                        | Logotipo a la izquierda y menú a la derecha, en una línea                                                                            |
| Portada           | Fondo de superficie. Texto y, debajo, la imagen (proporción 3:2)                                                | Texto en las columnas 1 a 7 e imagen en las 8 a 12, centrados en vertical                                                            |
| Qué puedes hacer  | Tarjetas en tantas columnas como quepan, de 256 px como mínimo (una en el móvil)                                | Tres columnas iguales                                                                                                                |
| Cifras            | Banda con fondo primario; las tres cifras, una debajo de otra                                                   | En fila, repartidas a lo ancho                                                                                                       |
| Próximas partidas | Lista de eventos, uno debajo de otro                                                                            | Tres columnas                                                                                                                        |
| Precios           | Uno debajo de otro                                                                                              | Tres columnas de la misma altura, con los botones alineados abajo                                                                    |
| Tabla             | Se desplaza en horizontal dentro de su caja; la página no                                                       | Todo el ancho, sin desplazamiento                                                                                                    |
| Pie               | Fondo primario oscuro; marca, horario, dirección y enlaces, uno debajo de otro; una línea encima de los enlaces | Dos columnas: la marca a la izquierda ocupando dos filas; el horario y la dirección a la derecha; los enlaces abajo, a todo el ancho |

Un solo punto de ruptura: **768 px (48 rem)**. Lo demás tiene que adaptarse solo, y la página no
puede desplazarse en horizontal en ningún ancho entre 320 y 1920 px.

## Imagen de la portada

En `img/` está la misma ilustración a tres anchos: `portada-480.jpg`, `portada-960.jpg` y
`portada-1440.jpg`. El navegador tiene que poder elegir la que necesite: en el móvil ocupa todo el
ancho y en escritorio, unas 5 de las 12 columnas.

## Tema oscuro

Se aplica cuando el sistema está en modo oscuro, solo en pantalla. Cambian solo los colores de la
tabla de colores que tienen valor en la columna «Tema oscuro», y la sombra desaparece. Todo lo demás
es igual.

## Impresión

En A4 con márgenes de 2 cm, texto negro sobre blanco y letra de 12 pt:

- Sin menú, botones, imagen de la portada ni iconos de las tarjetas. La cabecera no se queda fija.
- Las tarjetas y los precios, con un borde negro de 1 px, sin sombra, y nunca partidos entre dos
  hojas; tampoco las filas de la tabla. Sin el icono, la etiqueta «Novedad» va encima del título.
- La banda de cifras y el pie, sin fondo y en negro.
- La tabla se ve entera, sin desplazamiento.
- Un título nunca se queda solo al final de una hoja.
- Detrás de cada enlace externo, su dirección entre paréntesis.

## Clases del HTML

| Clase                                                                                                                      | Tipo                    | Qué es                                                                 |
| -------------------------------------------------------------------------------------------------------------------------- | ----------------------- | ---------------------------------------------------------------------- |
| `boton`                                                                                                                    | Componente              | Botón (es un enlace)                                                   |
| `boton-contorno`                                                                                                           | Modificador             | Botón sin fondo                                                        |
| `etiqueta`                                                                                                                 | Componente              | Etiqueta de texto pequeño                                              |
| `etiqueta-esquina`                                                                                                         | Modificador             | Etiqueta colocada en la esquina de su tarjeta                          |
| `etiqueta-completo`                                                                                                        | Modificador             | Etiqueta de plazas agotadas                                            |
| `tarjeta`, `tarjeta-icono`                                                                                                 | Componente y su parte   | Tarjeta de «Qué puedes hacer» y su icono                               |
| `logo`                                                                                                                     | Componente              | Logotipo (en la cabecera y en el pie)                                  |
| `menu`                                                                                                                     | Componente              | Menú principal                                                         |
| `eventos`, `evento`, `evento-fecha`, `evento-dia`, `evento-titulo`, `evento-datos`                                         | Componente y sus partes | Lista de próximas partidas                                             |
| `cifra`, `cifra-numero`                                                                                                    | Componente y su parte   | Cada cifra de la banda                                                 |
| `precio`, `precio-importe`, `precio-unidad`, `precio-lista`                                                                | Componente y sus partes | Tarjeta de precio                                                      |
| `precio-destacado`                                                                                                         | Modificador             | Precio destacado                                                       |
| `tabla`, `numero`                                                                                                          | Componente y su parte   | Tabla de torneos y sus celdas numéricas                                |
| `tabla-desplazable`                                                                                                        | Componente              | Caja que se desplaza si la tabla no cabe                               |
| `texto-suave`                                                                                                              | Utilidad                | Texto con el color suave                                               |
| `oculto-visual`                                                                                                            | Utilidad                | Texto solo para lectores de pantalla (el título de la banda de cifras) |
| `contenedor`, `seccion`                                                                                                    | Maquetación             | Ancho máximo centrado; relleno de las secciones                        |
| `cabecera`, `cabecera-contenido`                                                                                           | Maquetación             | Cabecera                                                               |
| `portada`, `portada-contenido`, `portada-texto`, `portada-imagen`, `antetitulo`, `titulo-portada`, `entradilla`, `botones` | Maquetación             | Zona destacada de la página de inicio                                  |
| `rejilla`                                                                                                                  | Maquetación             | Rejilla de tarjetas                                                    |
| `cifras`, `cifras-lista`                                                                                                   | Maquetación             | Banda de cifras                                                        |
| `precios`                                                                                                                  | Maquetación             | Rejilla de precios                                                     |
| `pie`, `pie-contenido`, `pie-marca`, `pie-horario`, `pie-contacto`, `pie-enlaces`, `pie-titulo`                            | Maquetación             | Pie                                                                    |

La entradilla de `torneos.html` usa la misma clase que la de la portada.

## Créditos

- Iconos: [Tabler Icons](https://tabler.io/icons), licencia MIT (ya están en el HTML).
- Tipografías: Fredoka y Nunito, de Google Fonts, licencia SIL Open Font License.
- Ilustración de la portada: hecha para el curso.
