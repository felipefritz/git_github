# Fundamentos Github

- Nube para almacenar repositorios y trabajar en colaboracion con otros.
- 
## Iniciar

### Asociar repositorio remoto a repositorio local
1. ```git remote add origin httpurlrepo``` : 
   1. ```remote```: fuente remota
   2. ```add```: agregar
   3. ```origin```: el nombre del remote

### Subir primer commit
1. Hacer commit y luego subir los cambios
2. ```git push -u origin master```
  1. ```origin```: nombre del repo
  2. ``` master:``` rama que deseamos
  3. ```-u```: ayuda a que la proxima vez que se quiera hacer push no se necesitara especificar la rama

### Traer cambios desde github a local:
1. ```git pull origin main ```
2. Si hay conflictos entre cambios de github y local, se debe configurar el pull:
3. ```git config pull.rebase true```

## Tags:
1. subir tags: ```git push –tags```
- Luego en github aparecera el boton de tags, en donde se pueden agregar comentarios presionando el hash del commit
  
## Release:
-  Son versiones del codigo q se crean a partir de tags
1. Pueden ser pre release: versiones beta
2. Release o version actual
   


# GITHUB opciones: 
1. fork: copiar un repositorio en repositorio personal
2. watch: darle seguimiento a un repo o proyecto
3. issues: seccion donde se separan preguntas o comentarios por etiquetas
4. actions: acciones automaticas que tiene github como desplegar sitios web, etc
5. projects: sirve para organizar proyectos y se pueden agregar items como pull requests

GB: Markdowns: Es un lenguaje similar a html para editar cuadros de texto en github
blame en archivo: es para saber que usuario hizo los cambios en algun archivo
