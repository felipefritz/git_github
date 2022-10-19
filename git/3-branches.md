# Branches
- Son lineas de tiempos de commits
- merge o uniones: une 2 ramas 
1. ```fast forward```: se dispara cuando no hay cambios en la rama principal a la cual se le quiere agregar ramas o cambios de otras ramas
2. ```uniones automaticas```: si rama principal tiene cambios y la otra rama no toca las lineas de la rama principal, esta se une automaticamente
3. ```union manual```: cuando la otra rama tiene conflictos con lineas de la rama principal, esto genera un conflico, se debe resolver de forma manual y git hace un commit nuevo con el nuevo merge.
   

- Crear ramas: <code>git branch nombreRama </code>
- Listar ramas: ```git branch```  (con * es la rama actual)
- Mover a otra rama: ```git checkout nombreRama```

### Unir Ramas ( fast forward)
1. Hacer cambios en la nueva rama (commits)
2. cambiarse a la rama master con git checkout master
3. ```git merge nombreRama```
- si no se necesita la rama, se puede eliminar con git branch -d nombreRama (-f para forzar la eliminacion )

- Crear rama y moverse a la nueva: git checkout -b nombreRama

### Conflicos en merges: 
- Cuando hay diferencias en el mismo archivo entre 2 ramas al hacer un push o pull
1. Se debe resolver manualmente ya que git no sabe cual version elegir
2. VSC muestra la comparacion de los archivos y se puede editar manualmente editando el archivo
3. Una vez resuelto el archivo a hacer commit, se debe hacer hacer un add y luego un commit
4. git add archivoConConflico git commit -m “union rama xxx”

