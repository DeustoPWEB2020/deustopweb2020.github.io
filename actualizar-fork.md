# Instrucciones para actualizar el fork en tu cuenta personal con las últimas modificaciones del repositorio central

Solamente la primera vez, tienes que indicar a tu repositorio personal dónde está ubicado el repositorio central. Para esto:

- Si lo estás haciendo para el repositorio de contenido adicional/trabajo con expertos:
    ```
    git remote add upstream https://github.com/DeustoPWEB2018/Elementos-de-la-UX.git
    ```

- Si lo estás haciendo para el repositorio del proyecto web de tu grupo:
    ```
    git remote add upstream https://github.com/TUNOMBREDEUSUARIO/proyectoweb-VUESTROTEMA.git
    ```

Después, cada vez que el repositorio central tenga cambios que quieres traer a tu copia personal:

1. Traer al branch master de tu ordenador los cambios que haya habido en el repositorio central:
    ```
    git pull upstream master
    ```

2. Actualizar también tu copia personal en la nube con estos cambios:
    ```
    git push origin master
    ```
    
3. Puede que quieras también borrar el branch sobre el que has estado trabajando, también en tu ordenador (porque ya has incorporado esos cambios a través del repositorio central)
    ```
    git branch -d NOMBREDEBRANCH
    ```