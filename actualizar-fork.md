# Instrucciones para actualizar tu copia local con las últimas modificaciones del repositorio central

<!--
Solamente la primera vez, tienes que indicar a tu repositorio personal dónde está ubicado el repositorio central. Para esto:

```
git remote add upstream https://github.com/TUNOMBREDEUSUARIO/proyectoweb-VUESTROTEMA.git
```

Después, -->

Cada vez que el repositorio central tenga cambios que quieres traer a tu copia personal:

1. Cámbiate al branch `master`:
```
git checkout master
```
2. Trae los cambios que ya se han incorporado en el repositorio central:
```
git pull origin master
```
3. Puede que quieras también borrar el branch sobre el que has estado trabajando, también en tu ordenador (porque ya has incorporado esos cambios a través del repositorio central)
```
git branch -D NOMBREDEBRANCH
```