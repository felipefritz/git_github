# REBASE: 
Sirve para:
- ordenar commits
- Corregir mensajes de los commits
- Unir commits
- Separar commits
- 
1. ```git rebase```: crea una espacio temporal de los commits de una rama distinta que estan en el mismo espacio que otro commit, y los pone en otro espacio de la linea.

No se debe utilizar cuando ya se hizo push.
	

Para hacer un rebase se debe hacer en la rama donde se quieren los cambios
Moverse a la rama que se quiere
git rebase master ( rama que se requiera
Es util para hacer merge entre 2 ramas y evitar conflictos, ya que añade los cambios del master a otra rama, y asi se evitarian conflictos al hacer merge. ya que la nueva rama ya tendra los cambios del master.
REBASE INTERACTIVO: git rebase -i HEAD~4 (o cantidad de commits anteriores
el ultimo de la lista es el ultimo commit
squash: fusionar dos commits en uno solo
al ejecutar el comando en i:  (SQUASH)
pick 338df10 Actualizamos dos misiones completadas al momento: cambiar pick por squash o s (en el commit que se quiera unir al commit anterior a ese de la lista )


renombrar mensaje de un commit con rebase
ejecutar i, luego en el pick cambiarlo a r y salir. esto nos permitira cambiar el mensaje
