# Guía de sintaxis de Markdown

Aquí tienes un resumen de la sintaxis de Markdown que puedes usar en cualquier sitio de GitHub.com o tus propios archivos de texto. Más información en la página de ayuda de GitHub [Basic Writing and Formatting Syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax/).

## Encabezados (títulos)

```
# Esto es una etiqueta <h1> 
## Esto es una etiqueta <h2>
###### Esto es una etiqueta <h6>
```

## Énfasis / resaltados

```
*Este texto estará en cursiva*
_Esto también estará en cursiva_

**Este texto estará en negrita**
__Esto también estará en negrita__

_Puedes **hacer** combinaciones_
```

*Este texto estará en cursiva*

_Esto también estará en cursiva_

**Este texto estará en negrita**

__Esto también estará en negrita__

_Puedes **hacer** combinaciones_

## Listas

### Desordenadas

```
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

* Item 1
* Item 2
  * Item 2a
  * Item 2b

### Ordenadas

```
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

## Imágenes

```
![Alt Text](url) por ejemplo:
![GitHub Logo](/img/octocat.png)
```

![GitHub Logo](/img/octocat.png)

## Enlaces

```
http://github.com - ¡automático!
[GitHub](http://github.com)
```

http://github.com - ¡automático!

[GitHub](http://github.com)

## Bloques de cita

```
Como dijo Kayne West:

> We're living the future so
> the present is our past.
```

Como dijo Kayne West:

> We're living the future so
> the present is our past.

## Código en línea

```
Creo que deberías usar
un elemento `<addr>` aquí.
```

Creo que deberías usar
un elemento `<addr>` aquí.

# Markdown con sabor GitHub

GitHub.com utiliza su propia versión de la sintaxis de Markdown que ofrece unas características adicionales muy útiles, muchas de las cuales hacen que trabajar con el contenido en GitHub.com sea más fácil.

Ten en cuenta que algunas de las características de Markdown con sabor GitHub sólo están disponibles en las descripciones y comentarios de Issues y Pull Requests. Éstas incluyen @menciones además de referencias a otros Issues y Pull Requests, entre otros.

Algunas de estas características son específicas para trabajar con código de desarrollo de software, por lo que no las recogeremos aquí (podéis verlas todas en [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)).

## Listas de tareas

Si incluyes una lista de tareas en el primer comentario de un Issue, obtendrás un práctico indicador de progreso en tu lista de issues. ¡También funciona en los Pull Requests!

```
- [x] soportan @menciones, #referencias, [enlaces](), **formato** y <del>etiquetas</del> 
- [x] requiere sintaxis de lista (soporta cualquiern lista ordenada o desordenada)
- [x] éste es un item completado
- [ ] éste es un item sin completar
```

- [x] soportan @menciones, #referencias, [enlaces](), **formato** y <del>etiquetas</del> 
- [x] requiere sintaxis de lista (soporta cualquiern lista ordenada o desordenada)
- [x] éste es un item completado
- [ ] éste es un item sin completar

## Tablas

Puedes crear tablas mediante listas de palabras separadas con guiones `-` (para la primera línea), y luego separando cada columna con una raya `|` (`AltGr+1`)

```
Primer encabezado | Segundo encabezado
------------ | -------------
Contenido de la celda 1 | Contenido de la celda 2
Contenido en la primera columna | Contenido en la segunda columna
```

Primer encabezado | Segundo encabezado
------------ | -------------
Contenido de la celda 1 | Contenido de la celda 2
Contenido en la primera columna | Contenido en la segunda columna

## Referencias a Issues del mismo repositorio

Cualquier número que haga referencia a un Issue o Pull Request será automáticamente convertido en un enlace.

```
#1
mojombo#1
mojombo/github-flavored-markdown#1
```

## @menciones a usuarios

Escribiendo una arroba `@` seguida por un nombre de usuario, se notificará a esa persona para que consulte el comentario. Esto se llama "@mención", porque estás _mencionando_ a la persona. También puedes hacer una @mención a equipos dentro de una organización.

## Enlaces automáticos de URLs

Cualquier URL (como http://www.github.com/) se convertirá automáticamente en un enlace clicable.

## Tachados

Cualquier palabra rodeada de dos tildes (`~~así~~`, con `AltGr+4`) aparecerá tachada, ~~así~~.

## Emoticonos

GitHub soporta emoticonos! :sparkles: :camel: :boom:

Para ver una lista de todos los emoticonos disponibles, mira el [Emoji Cheat Sheet](http://www.emoji-cheat-sheet.com/).