# Problema 4: animación web de programación lineal

Esta versión integra la gráfica, los estilos, las explicaciones y los
controles y documentos descargables en un único archivo `index.html`.
El PDF y el código LaTeX están incluidos en el HTML y se descargan
con el nombre y el tipo de archivo correctos, sin depender de rutas externas.

## Probar antes de publicar

1. Extrae TODO el ZIP.
2. Entra en `Problema_4_Web_Corregido`, donde se ve `index.html`.
3. Haz doble clic en `index.html`.

La animación se abre directamente en el navegador. No hace falta instalar
Python, Node, bibliotecas ni extensiones para usar esta página web.

## Qué incluye

- 12 pasos explicativos.
- Las dos restricciones y su región factible.
- Intersecciones y coordenadas.
- Tabla con los ingresos de cada vértice.
- Deslizador y reproducción de la recta de ingresos.
- Enunciado completo.
- PDF didáctico de nueve páginas y su código LaTeX, incluidos dentro del HTML.
- Configuración de GitHub Actions para publicar la versión del código subida.

## Corregir el botón de descarga en un repositorio existente

Sube el nuevo index.html a la raíz del repositorio, reemplazando el anterior,
y guarda con Commit changes en main. Tras publicarse, abre la web con
Ctrl+F5. El botón Descargar PDF descargará solucion-didactica.pdf.

## Publicar esta versión

Sigue `PASOS_PARA_PUBLICAR.md`.

En esta versión se utiliza **Settings > Pages > Source > GitHub Actions**.
El archivo que configura la publicación está en
`.github/workflows/publicar.yml`.

Para facilitar su creación desde la web de GitHub, se incluye también
una copia visible llamada `publicar.yml`. Esa copia por sí sola no se
ejecuta: debe existir en la ruta `.github/workflows/publicar.yml`.

La publicación comprueba que están presentes la animación y los documentos incluidos.
Si faltan, informa del problema en Actions en vez de publicar una página
incompleta basada solamente en el README.

## Archivos de la web

| Archivo | Uso |
| --- | --- |
| `index.html` | Página completa: diseño, gráfica, lógica y animación. |
| `materiales/solucion-didactica.pdf` | Solución didáctica descargable. |
| `materiales/solucion.tex` | Código LaTeX del documento. |
| `.github/workflows/publicar.yml` | Publicación automática en GitHub Pages. |
| `publicar.yml` | Copia visible del archivo de publicación para copiarlo en GitHub. |
| `PASOS_PARA_PUBLICAR.md` | Guía de publicación desde cero. |

## Resultado matemático

Maximizar Z = 0.30x + 0.60y, con:

- 6x + 12y <= 18000 libras.
- 3x + y <= 1800 pies cúbicos.
- x, y >= 0 y enteros.

Una carga óptima es 120 contenedores de Smith y 1440 de Johnson.
El ingreso máximo es $900 por camión y viaje. Hay 61 combinaciones
enteras óptimas en total.

## PDF y LaTeX

La web descarga el PDF ya compilado que está incluido dentro de index.html.
La carpeta materiales contiene copias para editar o consultar. Si cambias
esos documentos, también debes volver a incluir las nuevas versiones en
index.html: sustituir solamente la carpeta no cambia las descargas del HTML.

Este paquete no crea ni elimina repositorios por sí solo. El enlace real
aparecerá cuando GitHub termine de publicar el contenido de tu repositorio.

## Colores del tema

La barra superior incluye el selector Tema: Verde, Azul, Violeta, Coral
y Oscuro. La elección se guarda en el navegador cuando este lo permite.
El cambio de tema no modifica las restricciones ni los cálculos.
