 # Stash
 
 - Descripcion: Es un lugar donde se pueden mover todos los cambios, estaran de manera segura desde el utlimo commit. Luego se podra seguir trabajando con esos cambios.
Esto se aplica para cuando se requiere hacer un deploy, y mantener todo el codigo  nuevo almacenado en un stash, una vez realizado el deploy, se puede retomar el codigo almacenado. 
Es similar a una rama.

1. ```git stash```: Guarda todos los archivos del directorio, esto entrega un hash en el log
2. Ver stashes: ```git stash list```
4. Tomar el ultimo stash: ```git stash pop``` ( elimina el ultimo stash)
luego con el codigo retomado, se puede hacer un git commit.

5. Agregar stash con msje: ```git stash save “mensaje”```


### Conflictos con el stash
- Si un archivo es modificado luego de hacer git stash, se puede modificar ese archivo y agregarle cosas, luego al retomar el stash tendra las cosas del stash mas las nuevas cosas agregadas ( similar a merge conflicts) (automerge).
- Si hay conflictos se deben solucionar de manera manual (deben estar los cambios con commit
1. Limpiar stash: ```git stash clear```
2. Listar stash: ```git stash list```
3. Recuperar un stash especifico: ```git stash apply idStash```
4. Eliminar un stash de la lista: ```git stash drop idStash```
5. ver stash: ```git stash show idStash```
