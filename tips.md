## Preparando un repo para viajes en el tiempo

- ```git reset –soft HEAD^```: Esto me posisiona en el commit anterior para poder editarlo, para ir a un commit especifico cambiar HEAD^ por el id del commit, ( se saca de git log)

#### Para ir a un commit especifico y eliminar los siguientes:
- ```git reset –hard idCommit```
- ```git reflog```: muestra un historico de todo: reset, commits , etc
- 
### Ir a un commit eliminado: 
- se debe sacar desde git reflog el ID del commit
- ejecutar: ```git reset –hard idCommitEliminado```
- ```git mv nombrearchivo nuevonombre```: Cambiar nombre o eliminar

- ```git rm nombreArchivo```: Eliminar archivo en commit
#### Cambiar nombre fuera de git
1. Se elimina desde el directorio y git lo registrara
2. luego ```git add . ```
3. luego verificar con ```git status```
4. ```git commit -m “hacer el commit para registrar “```
