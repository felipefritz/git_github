## Cambio en los archivos

```git diff ```: 

Muestra la diferencia de algun archivo modificado, pero si el archivo fue modificado y agregado al commit, este no se vera. Para ver las diferencias se pueden desde vscode en sourcecontrol y pinchar el archivo

#### Editar comentarios de un commit: 
1. ```git log``` para ver los ultimos commits
2. ```git commit –amend -m “nuevo mensaje” ```: editar comentario

### Preparando un repo para viajes en el tiempo
1. ```git init```
2.```git add README.md```
3. ```git commit -m “readme agregado” ```
4. ```git add file1.txt file2.txt ```:  ir agregando archivos md por uno a uno
5. ```git add carpeta/ ``` ->  luego hacer commit.
6. ```git reset –soft HEAD^```  → Esto posiciona en el commit anterior para poder editarlo, para ir a un commit especifico cambiar HEAD^ por el id del commit, ( se saca de git log)

### Para ir a un commit especifico y eliminarlo:
 ```git reset –hard idCommit ```

```git reflog ```: muestra un historico de todo: reset, commits , etc

### Ir a un commit eliminado: 
1. se debe sacar desde ```git reflog``` el ID del commit
2. ejecutar: ```git reset –hard idCommitEliminado```
3. Cambiar nombre o eliminar
4. ```git mv nombrearchivo  nuevoNombre```
   

```git rm nombreArchivo```: Eliminar archivo en commit

### Cambiar nombre fuera de git
1. Se elimina desde el directorio y git lo registrara
2. luego git add . 
3. luego verificar con git status
4. git commit -m “hacer el commit para registrar “


#### Ignorar archivos o directorios que no queremos
1. crear fichero .gitignore en la raiz
    1. para carpetas: caperta/
    2. para ficheros: nombre.py
    3. para todos los archivos con extension en la raiz: *.py 
    4. archivos con extension dentro de directorio carpeta/*.py


### git reset [Referencia](https://www.freecodecamp.org/espanol/news/la-guia-definitiva-para-git-reset-y-git-revert/)

