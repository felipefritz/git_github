# REBASE: 
Es util para hacer merge entre 2 ramas y evitar conflictos, ya que añade los cambios del master a otra rama, y asi se evitarian conflictos al hacer merge. ya que la nueva rama ya tendra los cambios del master.

- Es una forma de mover la totalidad de una rama a otro punto del árbol.

- Para realizar rebase, asegúrate de tener todos los commits que quieras en el rebase en tu rama master. Revisar la rama en la que quieres hacer el rebase y escribe ```git rebase master``` (donde master es la rama en la que quieres hacer el rebase).
  
- sólo debes ejecutar git rebase en un repositorio local.

Sirve para:
- ordenar commits
- Corregir mensajes de los commits
- Unir commits
- Separar commits
  
### Como usar rebase:
1. Se debe estar en la rama a la cual se le quieren agregar los cambios de otra rama ( ```git checkout nombreRama```)
2. ```git rebase feature/add_file``` ( o nombre rama a unir al master)
3. Validar cambios con ```git checkout ramaIntegrada``` -> ```git merge master```
4. Moverse a la rama master y eliminar rama integrada con ```git branch -d nombreRama```

No se debe utilizar cuando ya se hizo push.

### REBASE INTERACTIVO:
- Es un rebase en donde se abre un archivo en el terminal el cual se puede editar.
- 
 1. ```git rebase -i HEAD~2``` (o cantidad de commits anteriores)
    1. -i: interactivo
    2. HEAD~2: numero de commits (2)
    3. Tambien se le puede pasar el id del commit


 2. Dentro del archivo interactivo:
    1. Presionar letra a para editar el archivo
    2. pick: son los ultimos commit y se pueden editar los mensajes del commit
    3. squash (s): Toma 2 commits y los fusiona.
       1. Para usar squash se debe cambiar pick del ultimo commit por squash o s.
       2. Esto lo que hara es fusionar los ultimos 2 commit


- el ultimo de la lista es el ultimo commit
- squash: fusionar dos commits en uno solo
- al ejecutar el comando en i:  (SQUASH)
-  ```pick 338df10 ```  al momento: cambiar pick por squash o s (en el commit que se quiera unir al commit anterior a ese de la lista )


renombrar mensaje de un commit con rebase
ejecutar i, luego en el pick cambiarlo a r y salir. esto nos permitira cambiar el mensaje


Si hay conflictos entre cambios de github y local, se debe configurar el pull:
git config pull.rebase true
