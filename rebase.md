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
  

1. ```git rebase```: crea una espacio temporal de los commits de una rama distinta que estan en el mismo espacio que otro commit, y los pone en otro espacio de la linea.

	
Para hacer un rebase se debe crear en la rama donde se quieren los cambios
1. Moverse a la rama que se quiere usando ```git checkout rama```
2. ```git rebase master``` ( o la -rama que se requiera)

No se debe utilizar cuando ya se hizo push.


### REBASE INTERACTIVO:
 ```git rebase -i HEAD~4``` (o cantidad de commits anteriores)
- el ultimo de la lista es el ultimo commit
- squash: fusionar dos commits en uno solo
- al ejecutar el comando en i:  (SQUASH)
-  ```pick 338df10 ```  al momento: cambiar pick por squash o s (en el commit que se quiera unir al commit anterior a ese de la lista )


renombrar mensaje de un commit con rebase
ejecutar i, luego en el pick cambiarlo a r y salir. esto nos permitira cambiar el mensaje


Si hay conflictos entre cambios de github y local, se debe configurar el pull:
git config pull.rebase true
