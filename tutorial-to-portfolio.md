# Paso a paso: del tutorial "Comunicar con Markdown" a mi portafolio personal para la asignatura

Si tienes cualquier problema al llevar a cabo estos pasos, envíame un email o mencióname (escribiendo `@mberasategi`) en cualquier issue o pull request de tu repositorio explicando el problema.

## Paso 1. Renombrar el repositorio

Vamos a configurar tu repositorio del tutorial "Comunicar usando Markdown" (en http://github.com/TUNOMBREDEUSUARIO/portafolio-markdown/ o http://github.com/TUNOMBREDEUSUARIO/markdown-portfolio/, si lo has hecho en inglés) para que funcione como vuestra página personal en GitHub y sirva como portafolio del trabajo individual que hacéis en la asignatura Proyectos para la web. Para esto, lo primero es renombrar el repositorio.

Accede a la pestaña **Settings** y en "Repository name", cambia el nombre a:

```
<tunombredeusuario>.github.io
```

y haz clic en **Rename**.

Una vez lo hayas hecho, puedes acceder a tu portafolio desde http://tunombredeusuario.github.io

## Paso 2. Revertir a página principal por defecto

<!-- Editar index.md, renombrar a tutorial.md
Editar contenido de README.md para añadir una intro al portafolio

--- 
task: new issue
title: Paso 2. Configurar la página principal
content: -->

Durante el tutorial has añadido una serie de elementos (títulos, imágenes, listas etc.) que se muestran en la página principal del sitio web. Vamos a cambiar esos contenidos a otra página, para configurar una página principal que tenga más sentido. 

<!-- 1. Fíjate en el número de este issue: lo verás al lado del título del issue (por ejemplo, `#6`) -->
2. En la pestaña **Code** de tu repositorio, haz clic en el archivo `index.md`
6. Haz clic en el icono del lápiz (parte derecha) para editar el archivo
7. En la parte superior, cambia el nombre del archivo de `index.md` a `tutorial.md`
8. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
9. Asegúrate de seleccionar "Create a new branch for this commit and start a pull request." y nombra el branch `pagina-principal`
<!-- 10. En la ventana para crear un nuevo pull request, escribe lo siguiente: `closes #6` utilizando el número del issue que memorizaste en el primer punto -->
12. Haz clic en "Create pull request"


Cuando se combine el branch `pagina-principal`, tal y como está ahora la página principal de tu sitio mostraría el contenido del archivo `README.md`. Este repositorio empezó como parte de un tutorial, para el que la descripción que tienes ahora en el archivo `README` tenía sentido. Pero ahora, que queremos hacer de este sitio tu portafolio personal, debería contener una frase o un párrafo corto acerca de lo que es (tu portafolio personal para la asignatura _Proyectos para la web_).

1. En la pestaña **Code** de este repositorio, selecciona el branch `pagina-principal` 
2. Accede al archivo `README.md` y haz clic en el icono del lápiz para editar el archivo
2. Elimina todo el texto que hay en ese archivo y escribe tu frase o párrafo corto de presentación para tu portafolio personal
3. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
4. Asegúrate de seleccionar "Commit directly to the `pagina-principal` branch." y haz clic en "Commit changes"

Puedes volver a hacer cambios todas las veces que quieras, simplemente asegúrate de guardarlos en el branch `pagina-principal`. Ten en cuenta que esta descripción aparecerá en la parte superior de tu sitio web, así que quizá quieras tenerlo en cuenta a la hora de decidir cómo redactarla.

Cuando hayas terminado y estés lista para publicar los cambios, vamos a incorporar estos cambios al branch que se publica como sitio web, `master`:

1. En la página del pull request que has creado antes, haz clic en "Merge pull request" y luego en "Confirm merge"
2. Cuando todo haya ido bien, haz clic en "Delete branch"

## Paso 3. Personalizar información personal en config

Durante el tutorial se ha generado un archivo de configuración que contiene el título del sitio web y el tema (aspecto) que utiliza. Vamos a personalizar y a añadir algo más de información a esa configuración.

2. En la pestaña **Code** de tu repositorio, haz clic en el archivo `config.yml`
3. Haz clic en el icono del lápiz (parte derecha) para editar el archivo
4. En la primera línea, sustituye el título (`title: Welcome to my portfolio!`) por algo como `title: Portafolio de Nombre Apellido`
5. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
6. Asegúrate de seleccionar "Create a new branch for this commit and start a pull request." y nombra el branch `config`
12. Haz clic en "Create pull request"

Además de personalizar el título, vamos a añadir algo más de información al archivo de configuración. 

1. En la pestaña **Files changed** del pull request que acabas de crear, haz clic en los puntos suspensivos `...` al lado de `config.yml` para editar el archivo
2. A partir de la línea 2 (después del título, y antes de la línea que empieza con `theme: `) copia y pega lo siguiente:

```
description: Mismo texto que en el archivo README
author:
  name: Nombre Apellido
  email: nombre.apellido@opendeusto.es
  links:
    - title: Twitter
      url: https://twitter.com/tu-usuario
      icon: fab fa-twitter-square
    - title: Instagram
      url: https://instagram.com/tu-usuario
      icon: fab fa-instagram
    - title: GitHub
      url: https://github.com/tu-usuario
      icon: fab fa-github-square
```

3. Personalízalo con tu información (descripción, nombre, email etc.)
4. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
4. Asegúrate de seleccionar "Commit directly to the `config` branch." y haz clic en "Commit changes"

Puedes volver a hacer cambios todas las veces que quieras, simplemente asegúrate de guardarlos en el branch `config`. Puedes añadir enlaces a tus perfiles de Twitter e Instagram, además del de GitHub. Si no quieres añadir alguno de ellos, simplemente elimina las tres líneas correspondientes.

Cuando hayas terminado y estés lista para publicar los cambios, puedes incorporarlos al branch que se publica, `master`:

1. Haz clic en "Merge pull request" y luego en "Confirm merge"
2. Cuando todo haya ido bien, haz clic en "Delete branch"

## Paso 4. Crear primer post

Vuestro portafolio personal incluirá actualizaciones periódicas en forma de blog con las anotaciones que hagáis de las lecturas individuales. Para esto, vamos a crear el primer post, que servirá de ejemplo para crear los siguientes.

2. En la pestaña **Code** de tu repositorio, haz clic en "Create new file"
3. En el campo del nombre de archivo, nómbralo así: `_posts/2019-10-10-mi-primer-post.md`
4. Los archivos de post deben tener este formato: 

```
---
title: Título del post
date: 2019-10-10
---

Texto del post
```

5. Copia y pega ese texto, y escribe un texto de prueba donde dice "Texto del post".
5. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
6. Asegúrate de seleccionar "Create a new branch for this commit and start a pull request." y nombra el branch `convertir-en-blog`
12. Haz clic en "Create pull request"

Una vez que tengas terminado el contenido de prueba que quieras añadir a tu primer post, puedes puedes incorporar los cambios al branch que se publica, `master`:

1. Haz clic en "Merge pull request" y luego en "Confirm merge"
2. Cuando todo haya ido bien, haz clic en "Delete branch"

De momento, el post que acabas de crear no se ve en ningún sitio, porque el tema (aspecto) que aplicaste en el tutorial no está preparado para alojar blogs. En el siguiente paso cambiaremos esto.

## Paso 5. Elegir un tema para el blog

Accede a https://jekyllthemes.io/jekyll-blog-themes y revisa los temas preparados para mostrar blogs. Elige uno que te guste (y que sea gratuito). Algunos de los más populares son [Minimal Mistakes](https://jekyllthemes.io/theme/minimal-mistakes), [Beautiful Jekyll](https://jekyllthemes.io/theme/beautiful-jekyll) y [Hyde](https://jekyllthemes.io/theme/hyde).

Una vez hayas escogido el tema que te gusta, accede a su repositorio en GitHub (haz clic en el botón "Get NOMBREDELTEMA on GitHub"), por ejemplo, https://github.com/poole/hyde. Anota el usuario/repositorio del tema escogido, en este ejemplo, `poole/hyde`.

2. En la pestaña **Code** de tu repositorio, haz clic en el archivo `config.yml`
3. Haz clic en el icono del lápiz (parte derecha) para editar el archivo
4. Elimina la línea que dice `theme: jekyll-theme-cayman` y escribe en su lugar la referencia al repositorio remoto que contiene el tema que has elegido. En el caso del ejemplo anterior, lo siguiente: 

```
remote_theme: poole/hyde
```

5. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
6. Asegúrate de seleccionar "Commit directly to the `master` branch." 
12. Haz clic en "Commit changes"

Espera un momento a que se reconstruya tu página, y en breve podrás ver tu nuevo sitio en tunombredeusuario.github.io

## Paso 6. Crear un post para las lecturas de la semana pasada

A partir de ahora, además de poner en común las lecturas individuales en clase, tendréis que crear un post en vuestro sitio web resumiendo o recogiendo vuestras anotaciones para cada una de estas lecturas. De momento, empezad con las lecturas de la semana pasada. Los pasos para crear un nuevo post serán siempre los mismos:

2. En la pestaña **Code** de tu repositorio, haz clic en "Create new file"
3. En el campo del nombre de archivo, nómbralo así: `_posts/2019-10-10-mi-primer-post.md`. Esto creará el nuevo archivo dentro de la carpeta `_posts`
4. Los archivos de post deben tener este formato: 

```
---
title: Título del post
date: 2019-10-10
---

Texto del post
```

5. Copia y pega ese texto, modifica el título y la fecha del post, y escribe tus anotaciones para las lecturas donde dice "Texto del post".
6. Formatea el texto usando la sintaxis Markdown (títulos, negritas/cursivas, listas, citas...)
5. Haz scroll hasta la parte inferior de la página y escribe un mensaje de commit descriptivo
6. Asegúrate de seleccionar "Commit directly to the `master` branch." 
12. Haz clic en "Commit changes"
