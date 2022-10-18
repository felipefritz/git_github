# SECCION 1: Fundamentos: Comandos
## Variables en comandos:
- simbolo - : abreviatura
- simbolo –- : palabra

### Comandos de inicio

- ``` git –version```: version de git
- ```git help```: ayuda
- ```git help nombrecomando```: entrega ayuda sobre el comando especifico, ej git help commit. Una ve dentro presionar q para salir

### Configurar usuario global:
- ```git config –global user.name “nombreusuario”```: Configura el usuario global de git
- ```git config –global user.email “email”```: Configura el email global de git
- ```git –global –e ```: Muestra los datos configurados en git global

### Iniciar Repositorio y primer commit: 
- ```git init```: Inicia un repositorio
- ```git status```: Entrega un estado actual de los commits
- ```git reset nombrearchivo o *.extension```: para excluir archivos del stage
- ```git reset .nombreArchivo ```: Quita el archivo del stage
- ```git commit -m “nombre commit”```: Hacer commit sin agregar archivo ```-m``` -> mensaje
- ```git commit -am “mensaje”``` : Agrega los archivos y hace el commit

### Agregar archivos al stage:
- ```git add .``` : Agrega todos los archivos ```.``` -> Todos los archivos
- ```git add nombreArchivo```: Agrear al stage solo un archivo 
- ```git add "*.txt"```:  agrega todos los archivos txt de todo el proyecto
- ```git add carpeta/*.txt```: Agrega todos los txt de un directorio
- ```git add carpeta/```: Agrega todos los archivos y subdirectorios dentro de la carpeta.
- ```git add nombrearchivo.html archivo2.html```: Agrega multiple archivos


#### Agregar carpeta vacia:
- dentro de la carpeta vacia agregar el archivo .gitkeep
- ```git add carpeta/.gitkeep```: Agregar .gitkeep al commit: 

#### Si un archivo se edita por error y no deja volver atras con control z, se puede recuperar desde el ultimo commit:
-```git checkout – .```: Reconstruir proyecto al ultimo commit: 

### Alias a los shortcuts
- ```git config –global alias.nombreAlias shorcutAcambiar```
- ejemplo: ```git config –global alias.s status –short```

# RAMAS: branch
- ```git branch ```: muestra todas las ramas y con * muestra la rama actual
- ```git branch -m nombreRama nombreNuevaRama ```: cambiar nombre rama: 
- ```git config –global init.defaultBranch nombreNuevaRama ```: cambiarn nombre rama global para todos los repo
- 
### GIT LOGS:
- ```git log ```: Muestra el historial de commits y sus ramas
- ```git log –oneline --graph ```: Muestra el historial de commits en una linea con un grafico de branches

### Cambios en los archivos
```git diff``` : Muestra la diferencia de algun archivo modificado, pero si el archivo fue modificado y agregado al commit, este no se vera. Para ver las diferencias se pueden desde vscode en sourcecontrol y pinchar el archivo.

### Editar comentarios de un commit: 
-```git commit –amend -m “nuevo mensaje”``` editar comentario del útlimo commit

