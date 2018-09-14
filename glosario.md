# Glosario de términos para trabajar con git/GitHub

repository
: Un **repositorio** es el elemento más básico de GitHub. Es más fácil imaginarlos como carpetas de proyecto. Un repositorio contiene todos los archivos de un proyecto (incluyendo la documentación), y almacena el histórico de modificaciones de cada archivo. Los repositorios pueden tener múltiples colaboradores y pueden ser tanto públicos como privados.

commit
: Un commit se puede entender como la **confirmación** de una modificación individual en un archivo (o serie de archivos). Es como cuando guardas un archivo, excepto que con Git, cada vez que haces commit se crea un ID único (también conocido como SHA o _hash_) que te permite registrar qué cambios se hicieron y quién los hizo. Los commits generalmente contienen un mensaje de commit que consiste en una breve descripción de los cambios realizados. 

push
: Literalmente, **empujar**. Se refiere a enviar tus cambios confirmados (tus commits) a un repositorio remoto, como por ejemplo un repositorio alojado en GitHub. Si cambias algo localmente, querrás hacer push de esos cambios para que los demás miembros de tu equipo puedan acceder a ellos.

pull
: Literalmente, **tirar**. Se refiere a _traer_ los cambios del servidor remoto y combinarlos con tu copia local. Por ejemplo, si alguien ha editado el archivo remoto en el que ambos estáis trabajando, querrás hacer pull de esos cambios a tu copia local para que esté actualizada.

issue
: Los issues son sugerencias de mejora, tareas o cuestiones relacionadas con el repositorio o el proyecto. Cualquiera puede crear issues (en un repositorio público), y los moderan los colaboradores del repositorio. Cada issue contiene su propio foro de dissusión, y se puede etiquetar y asignar a un usuario.

pull request
: Los pull requests o, literalmente, **solicitudes de tirar**, son cambios propuestos para un repositorio que un usuario ha enviado, y que pueden ser aceptados o rechazados por los colaboradores del repositorio. Igual que los issues, los pull requests tienen cada uno su propio foro de discusión.

branch
: Un branch o, literalmente, **rama**, es una versión paralela de un repositorio. Está contenido _dentro_ del repositorio, pero no afecta al branch principal o `master`, permitiéndote trabajar libremente sin estropear la versión "real". Cuando has terminado de realizar los cambios que querías hacer, puedes hacer merge de tu branch al branch principal para publicar tus cambios.

merge
: Literalmente, **combinar**. Hacer merge toma los cambios de un branch (en el mismo repositorio o también desde un fork), y los aplica en otro. Esto a menudo ocurre como un pull request (que se puede entender como una solicitud de hacer merge), o a través de la línea de comandos. Un merge puede realizarse automáticamente a través de un pull request en la interfaz web de GitHub siempre y cuando no haya cambios que generen conflictos, o puede hacerse siempre via línea de comandos.

remote
: La versión **remota** es una versión de algo que está alojada en un servidor, muy probablemente GitHub en este contexto. Puede estar conectado a clones locales de forma que los cambios se sincronicen.

local
: La versión **local** es la copia que tienes del repositorio en tu ordenador, sobre la que trabajas. 

clone
: Un **clon** es la copia de un repositorio que se aloja en tu ordenador, en lugar de en un servidor en alguna parte, o el acto de realizar esa copia. En tu clone puedes editar los archivos en tu editor preferido y utilizar Git para llevar un registro de esas modificaciones sin necesidad de tener conexión a internet. Sin embargo, este clon está conectado a la versión remota de forma que los cambios se puedan sincronizar entre ambos. Puedes hacer push de tus cambios locales a la versión remota para mantenerlas sincronizadas cuando estés online.

fork
: Un fork o, literalmente, **tenedor**, es una copia personal de un repositorio de otro usuario que se aloja en tu cuenta. Los forks te permiten modificar libremente cualquier proyecto sin alterar el original. Los forks se mantienen relacionados con el original, de manera que puedes enviar un pull request al autor del repositorio original para que lo actualice con tus cambios. También puedes mantener tu fork actualizado haciendo pull de las modificaciones del original.