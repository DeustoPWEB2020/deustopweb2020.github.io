# Git para usuarios de Dropbox (o Google Drive)
_forked from [magicseth/GitForDropboxUsers.md](https://gist.github.com/magicseth/1951984)_

## Git es genial

Puedes pensar en git como algo parecido a Dropbox: coge los archivos de tu ordenador, los pone en la nube, y permite que otras personas trabajen sobre ellos. Pero tiene algunas ventajas notables:

### Colaboración

Como Dropbox, git permite que varias personas trabajen en el mismo archivo al mismo tiempo. Esto es genial cuando varias personas están trabajando juntas en el mismo documento, o un grupo de personas están creando contenidos para un sitio web. Todos pueden estar contribuyendo a las mismas carpetas y archivos, sin miedo de sobreescribir el trabajo unos de otros, algo que en Dropbox puede ocurrir.

### Máquina del tiempo

Incluso si no tienes un equipo de personas, git sigue teniendo ventajas importantes. Puede funcionar como una máquina del tiempo, permitiéndote volver a ver lo que hiciste la semana pasada, o incluso el año pasado, ayudarte a recuperar archivos que borraste, y llevar un registro del progreso a lo largo del tiempo. Dispone de herramientas potentes que te permiten ver qué has ido cambiando a lo largo del tiempo.

### Y más

Git también es genial para hacer copias de seguridad para que no pierdas nada. Puede permitirte aprender acerca de tu forma de trabajar: ¿cuándo haces tu mejor trabajo? ¿Cada cuánto lo cambias todo? Existen herramientas para mostrar diferencias visuales entre versiones de imágenes, y todo tipo de cosas.

## Pero...

Git es genial... pero conceptualmente supone un salto desde el modelo mental de lo que es un archivo que maneja la mayoría de la gente.

Hay tantas razones estupendas para que los no-programadores utilicen Git cuando trabajan con otras personas, y me gustaría convencerte de que hay incluso más ventajas increíbles en la senda de git, pero no haré eso hoy. 

Mi objetivo para hoy:

> Proponer una analogía con Dropbox que ayude a perfiles no programadores entender el model mental de cómo funciona Git.

Puede ayudarte si piensas en ello como algo parecido a Dropbox, para empezar. Es como Dropbox, pero con un montón de pasos más. Ten fe (de momento) de que más pasos valen la pena, y te iré explicando las diferencias. 

Primero, una revisión rápida de cómo funciona Dropbox: varias personas pueden estar trabajando en el mismo archivo cada una en su ordenador, y mágicamente todos obtienen los cambios de los demás. En segundo plano, Dropbox está haciendo toda clase de cosas para que esto funcione. Con Git, acabas ayudando a hacer parte de este trabajo en segundo plano, y Git the lo agradece.

## Fácil como 4... 5... 6

Aquí tienes un modelo más explícito de cómo funciona Dropbox.

1. Instalas Dropbox
2. Alguien comparte una carpeta contigo
3. Tu ordenador descarga los contenidos de esa carpeta desde _la nube_
4. Haces algunos cambios a un archivo en la carpeta y los guardas
5. Tus cambios se suben inmediatamente a _la nube_ en Dropbox
6. Los cambios se descargan a los ordenadores de los demás inmediatamente

Bueno, esto es exactamente como Git. Solo que Git omite parte de la magia "inmediata". Los pasos 4, 5 y 6 no ocurren automáticamente: tienes que indicarle a Git cuándo quieres hacer cada paso. Vamos a desgranarlos.

### 4) Guardar... ¿seguro?

La primera diferencia es que Git no asume que tú quieras enviar cada cambio guardado a la nube. Te hace ser explícito acerca de qué es exactamente lo que quieres enviar a la nube.

> Mientras Dropbox sube automáticamente todo lo que guardas, Git añade un nuevo paso: la confirmación (o `commit` en lenguaje Git). Después de guardar un archivo, debes indicar a Git que quieres _confirmar_ ese cambio.

Para hacer esto, haces lo que se llama "staging". Esto realmente sólo significa decir a Git cuáles son los cambios de los que estás seguro. De esta forma, Git no hace perder el tiempo a los demás si haces un borrador que al final no te gusta.

### 5) Subir

Segunda diferencia: Dropbox sube tus archivos inmediatamente (o al menos lo intenta). Git no es tan impaciente para colocarlo todo en la nube.

> En Git, subir a la nube se llama `push`. Estás literalmente _empujando_ tus cambios desde tu ordenador a la nube. Sólo entonces podrán los demás descargarlos a sus propios ordenadores.

### 6) Descargar

La siguiente diferencia es la descarga. ¿Puedes imaginarte la diferencia? Efectivamente, mientras que Dropbox descarga los nuevos cambios automáticamente, Git espera a que tú se lo ordenes.

> Debes pedir explícitamente a Git que quieres _tirar_ de los cambios desde la nube (`pull` en lenguaje Git) a tu ordenador. Esto te trae la última copia completa de los documentos, incluyendo los cambios de todos los demás miembros del equipo.

Conserva la fe. Incluso si esto parece menos mágico, y más trabajo, existen razones para tomarse estas molestias.

### Ordenando, ¿o 6... 4... 6... 5...?

Git te requiere que funciones con un orden ligeramente diferente de operaciones porque es más manual (un poco menos mágico).

Antes de que empieces a hacer cambios, quieres asegurarte de que tienes al menos la última versión completa con los cambios del resto de tu equipo. Esto significa que lo primero que quieres hacer es descargar lo último desde la nube (dicho de otra forma, hacer un pull).

Ahora que ya tienes lo último, puedes cambiarlo y editarlo como quieras. Cuando estás satisfecho con tus cambios estás listo para decirle a Git que estás contento (o hacer un commit).

> También puedes repetir el paso 4 tantas veces como quieras, haciendo commit de pequeños cambios antes de pasar al siguiente paso.

Pero ¡espera un segundo! ¿Qué pasa si Sara de marketing ha cambiado el documento MIENTRAS tú estabas trabajando sobre él? Dado que Git no descarga los cambios automáticamente, tu ordenador (y, por extensión, tú) no tiene ni idea de que hay cambios. Así que esto añade un nuevo paso, re-descargar (o, hacer otro pull).

Bien, ahora Git conoce tus cambios, conoce los cambios de Sara, y lo único que queda por hacer es... ¡push! Finalmente podemos subir nuestros cambios a la nube para que todos los puedan ver.

### Esa es la esencia de Git

Es como Dropbox, pero tienes que decirle que descargue, guarde, descargue y suba cada vez (pull, stage y commit, pull y, finalmente, push).

Si lo llevas bien hasta aquí, veamos algunas diferencias algo más avanzadas.

## Diferencias avanzadas

Existen algunas diferenciás más en el modelo en el que se basan Git y Dropbox. La primera son los conflictos: qué pasa cuando dos personas cambian el mismo archivo. Otra importante es el hecho de que Git es "distribuido", es decir, no hay ninguna empresa que sea la única encargada de alojar tu contenido... puedes incluso tener múltiples nubes.

Aquí hay algunas revisiones rápidas de estas diferencias.

### Viaje en el tiempo

Cada commit hace una pequeña marca en una línea temporal. Git lleva un registro de CADA UNA de estas pequeñas marcas. Esto significa que puedes ir atrás en el tiempo, y ver cómo tu documento cambia desde el día 0 al presente. Puedes ver cada cambio, junto con quién lo hizo, y cuál fue el mensaje de commit. Bastante práctico.

> Git tiene "deshacer" de múltiples capas

Puedes descubrir exactamente quién escribió la errata y cuándo, y entonces corregirla realmente rápido (Git tiene algunas herramientas estupendas para esto también).
 
### Conflictos

¿Qué pasó cuando Sara cambió ese archivo en la nube, mientras tú trabajabas en el mismo archivo en tu ordenador? Dropbox se encarga de eso mágicamente en la nube, pero ahora -- es tu trabajo. El segundo paso 6 (volviendo a hacer pull desde la nube) en tu flujo de trabajo es cuando es más probable que tengas que "combinar (o `merge`) conflictos".

> Generalmente Git es bastante mágico y adivina qué hacer si Sara y tú estabais ambos editando el mismo archivo.

Por ejemplo si cambió el título del documento, y si tú añadiste algunas notas al pie, Git podrá resolverlo. Sin embargo, si tú cambias tu salario a 350.000e y Sara lo cambia a 40e, Git no va a saber qué hacer.

Si Sara hizo push de su cambio antes que tú, Git te pedirá que tú lo resuelvas. Te dirá: "Sara dice que tú cobras 40e la hora, pero tú dices que cobras 350.000e. ¿Quién tiene razón?". Tú decides. Resuélvelo, guárdalo (haz commit) y haz push. Pero asegúrate de hacer otro pull antes, por si Sara detectó el error y cambió tu tarifa a 400.000e mientras tú lo corregías.

### Meta comentarios

Cada vez que guardas (o haces commit, más bien) de algunos cambios, Git te pide un "mensaje de commit". Esto son un par de frases que describen los cambios que hiciste: un breve resumen para que alguien pudiera revisar la lista de cambios en este documento, sin tener que leerlo entero.

### Estilo

Como Git es un poco más manual, se sugieren unos pocos cambios estilísticos para que todo el mundo sea más feliz. Primero, pequeños cambios. Deberías hacer un commit cada vez que terminas de hacer una modificación parcial coherente. Por ejemplo, si estás cambiando tu salario, y el de Sara, primero haz un commit con tu ascenso y un mensaje de commit como "Ajustar el salario según méritos", y luego ajusta el salario de Sara con un mensaje de commit como "Equilibrar el presupuesto". Los buenos mensajes de commit (informativos) son muy apreciados en la comunidad Git.

Dada la naturaleza de resolver conflictos, Git también prefiere texto plano. Las imágenes son mucho más difíciles para Git (y para ti) de combinar (o merge) si dos personas las cambian a la vez. Así que cada vez que puedas, utiliza un formato de texto plano (como HTML o Markdown).

## Fin

Bueno, no sé si he conseguido convencerte de que TIENES QUE usar Git, pero espero que lo entiendas un poco mejor ahora. Si ya lo estás usando, espero que ahora tenga algo más de sentido. Por lo menos, estás un paso más cerca de convertirte en un compañero co-conspirador pro-Git.