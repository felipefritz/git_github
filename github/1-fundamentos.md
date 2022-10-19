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
1. fork: copiar un repositorio de otro usuario y en un repositorio personal
   1. Se clona el repo en nuestra cuenta de git y ahi se podran hacer modificaciones al repositorio de un tercero.
   2. El fork es como una rama adicional al repo original 
   3. Se puede hacer un pull request al repo original (contribuir a un proyecto)

2. watch: darle seguimiento a un repo o proyecto
3. issues: seccion donde se separan preguntas o comentarios por etiquetas
4. actions: acciones automaticas que tiene github como desplegar sitios web, CI/CD, etc
5. projects: sirve para organizar proyectos y se pueden agregar items como pull requests
6. Markdown: Es un lenguaje similar a html para editar cuadros de texto en github
7. blame en archivo: es para saber que usuario hizo los cambios en algun archivo

## Pull requests
- Son commits que deben solicitar autorizacion
- Se recomienda que los pull request se ejecuten desde local
- Al hacer un pull request desde github este crea una nueva rama propuesta
- Al hacer el pull request, este es notificado a las personas involucradas en el proyecto

### Aceptar un pull request: 
- Merge commit: se combinan con un commit adicional 
- squash: se tomaran los cambios y se fusionaran al ultimo commit

### Cancelar un pull request
#### Desde dueno del repo: 
2. ir a pestana pull requests
3. ir a files changed
4. click review changes
5. aca se podran agregar comentarios y solicitar request changes
#### Desde solicitante:
1. ir a pull requests
2. ir al changes requested y revisar que se debe modificar
3. ir al repo local
4. git log, tomar el id del commit antes de commit de los cambios solicitados
5. git checkout idcommit nombreArchivo
6. Hacer commit y push


## Github fetch:
- actualiza el repositorio local basado en todos los cambios realizados en la nube, se descargaran los nuevos commits al log, pero no actualiza los archivos
- Se utilizan antes de hacer un git pull para saber que es lo que hay en la nube antes de hacer un merge o un pull

## FLUJO DE GITHUB:
1. Crear el repo con rama principal
2. Desarrollar en otras ramas y hacer commits (Una rama para distintas funcionalidades)
3. Hacer pull requests para discutirlo con otros
4. Abrir discusion con otros usuarios y comentar con markdowns
5. Si esta todo OK, hacer el merge de la rama
6. Eliminar la rama
7. Siempre aceptar pull request de usuario verificados


## Flujos de trabajo
1. Cada desarrollador trabaja en un feature branch( una rama para cada uno). Pasos:
   1.  git fetch , para revisar los commits
   2.  git branch -a : para revisar todas las ramas en el repo
   3. git checkout : para pasarse a la rama de otra persona
   4. git checkout master: Para hacer el merge con otra rama o bien hacer un git push origin rama-x: Para subir toda la rama a github y hacer un pull request desde github


2. Subir ramas:
   1. No se pueden subir estando en la rama con un git push
   2. Subir ramas de esta manera: git push --set-upstream origin  nombreRama


3. Traer las ramas a local ( Pueden ser ramas de otra persona para revisarla):
   1. ```git pull –all```: esto no las mostrara en local 
   2. para mostrar las ramas en local: ```git branch -a```
   3. Cambiarse a otra rama:
   4. una vez identificada la rama: ```git checkout nombreRama```

4. Limpiar Ramas:
   1. ```git pull origin master```: para traer los merge y utlmos cambios en github
   2. ```git branch -d nombreRama```: elimina ramas locales no remotes
   3. eliminar una rama en local y en remote solo si existe en ambos lados:
        1. ```git push origin :rnombreRama```
   
   4. Eliminar rama si existe en local con git branch -a  pero no en remote:
      1. ```git remote prune origin```

## Rama produccion:
- Cuando se le da soporte a una version anterior:


1. crear una rama nueva y crear un tag en esa rama
2. hacer el ```git push –tag```
3. hacer un release a ese tag. Con esto hay un backup de la rama en caso de que sea eliminada
4. Restaurar rama a partir de un tag:
   1. hacer un git checkout a la rama desde local y hacer un git push para subir la rama
   2. Si la rama no existe en remote ni local ni en branch -a, nos podemos cambiar a la rama del tag:
      1. ```git checkout v1.0.0``` o la version deseada en github crear rama a partir de version
5. Eliminar rama en remote: ```git push origin :rama```



## Issues: 
- Se utilizan para hacer preguntas o hacer sugerencias a un repo
- Resolver issue por commit: git commit -am “Fixes #numeroissue: mensaje”
- Issue templates: en settings ->issues templates -> setup template
- wikis: Es una seccion que simula un sitio web del repositorio
## Proyectos:
-  Son como una pizarra en blanco donde se pueden gestionar tareas}
- Pueden ser pizarras tipo kanban o tablas

