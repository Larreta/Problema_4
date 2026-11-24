# Publicar desde cero: guía para esta versión corregida

## Paso 1. Extraer y probar

1. Descarga el ZIP corregido y selecciona **Extraer todo**.
2. Abre `Problema_4_Web_Corregido`, donde está `index.html`.
3. Haz doble clic en `index.html`. Debe aparecer la animación completa.

## Paso 2. Crear un repositorio nuevo

1. En GitHub, pulsa **+ > New repository**.
2. Puedes llamarlo `Problema_4` si ese nombre está libre. También puedes
   elegir `Problema_4_Web`, para conservar el repositorio anterior.
3. Selecciona **Public**.
4. Activa **Add README** para crear la rama `main`.
5. Pulsa **Create repository**.

## Paso 3. Subir la animación

1. En tu repositorio, pulsa **Add file > Upload files**.
2. Desde la carpeta extraída, arrastra:
   - `index.html`.
   - Opcionalmente, la carpeta `materiales` como copia de consulta.
     La descarga de PDF y LaTeX ya está incluida dentro de index.html.
   - `README.md` y `PASOS_PARA_PUBLICAR.md`.
3. Pulsa **Commit changes** y guarda en `main`.

Debes ver `index.html` directamente en la página principal del repositorio,
sin ninguna carpeta adicional por encima.

No subas únicamente el ZIP ni dejes otra carpeta por encima de index.html.
No necesitas subir los antiguos `app.js` y `styles.css`: esta versión
ya los lleva incorporados en index.html.

## Paso 4. Elegir el sistema de publicación

1. Entra en **Settings > Pages**.
2. En **Build and deployment > Source**, elige **GitHub Actions**.
3. Vuelve a la pestaña **Code** de tu repositorio.

Esta guía usa GitHub Actions. Sigue esa opción para que se ejecute el
archivo de publicación incluido en el paquete.

## Paso 5. Crear el archivo de publicación

1. En el repositorio, pulsa **Add file > Create new file**.
2. En el nombre escribe exactamente:

```text
.github/workflows/publicar.yml
```

GitHub irá creando los niveles de carpeta mientras escribes las barras.

3. En tu computadora, abre `publicar.yml`, el archivo visible del paquete,
   con VS Code o con el Bloc de notas.
4. Copia TODO su contenido y pégalo en el editor de GitHub.
5. Pulsa **Commit changes** y guarda en `main`.

También se incluye la ruta `.github/workflows/publicar.yml` completa
en el ZIP. Si ya la subiste manteniendo esa ruta, no hace falta crearla
de nuevo; solo comprueba que su contenido sea el del paquete.

## Paso 6. Esperar la publicación y obtener el enlace

1. Abre la pestaña **Actions**.
2. Selecciona **Publicar animacion web**.
3. Abre la ejecución más reciente y espera a que termine con un indicador
   verde. Debe corresponder al último cambio que acabas de guardar.
4. Si no se inició ninguna ejecución, pulsa **Run workflow**, selecciona
   la rama `main` y confirma **Run workflow**.
5. Vuelve a **Settings > Pages** y pulsa **Visit site**.

Ese es el enlace público que debes compartir.

Con la cuenta Larreta, si el repositorio se llama Problema_4,
el formato esperado será:

```text
https://larreta.github.io/Problema_4/
```

Si elegiste otro nombre de repositorio, el último tramo cambia.
El enlace no se crea por descargar este ZIP: debes completar la publicación.

## Si todavía aparece el título antiguo

- Comprueba que Source está en **GitHub Actions**.
- Revisa la ejecución MÁS RECIENTE de **Publicar animacion web**.
- Revisa que index.html contenga la animación completa.
- Ejecuta **Run workflow > main** para publicar la versión actual.
- Después de una publicación verde, abre Visit site y presiona Ctrl+F5.

No vuelvas a ejecutar una publicación antigua que corresponda al
primer commit del repositorio. Usa el nuevo workflow y la rama main.

## Si Actions muestra un error

Abre la ejecución, entra en el trabajo `publicar` y revisa el paso en rojo.
El paso de comprobación indica si falta index.html o si sus documentos incluidos no son válidos.
Si falla la configuración de Pages, comprueba de nuevo
**Settings > Pages > Source > GitHub Actions**.

## Fuentes oficiales

- https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Si la web ya se ve y solo falla el PDF

Sube únicamente el nuevo index.html a la raíz del repositorio y reemplaza
el anterior. Haz Commit changes en main y espera la publicación.
Abre la página con Ctrl+F5 y pulsa Descargar PDF. El archivo se llama
solucion-didactica.pdf y está incluido dentro del HTML; no necesita
la carpeta materiales para funcionar.

## Colores del tema

La barra superior incluye el selector Tema: Verde, Azul, Violeta, Coral
y Oscuro. La elección se guarda en el navegador cuando este lo permite.
El cambio de tema no modifica las restricciones ni los cálculos.
