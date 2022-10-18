

- Descripcion: El comando git merge fusionará cualquier cambio que se haya hecho en la base de código en una rama separada de tu rama actual como un nuevo commit.
- Cada vez que se ejecuta git merge, se crea un merge commit extra. Siempre que trabajes en tu repositorio local, tener demasiados merge commits puede hacer que el historia del commits parezca confuso. Una forma de evitar el merge commit es usar git rebase en su lugar.
  
1. ```fast forward```: se dispara cuando no hay cambios en la rama principal a la cual se le quiere agregar ramas o cambios de otras ramas
2. ```uniones automaticas```: si rama principal tiene cambios y la otra rama no toca las lineas de la rama principal, esta se une automaticamente
3. ```union manual```: cuando la otra rama tiene conflictos con lineas de la rama principal, esto genera un conflico, se debe resolver de forma manual y git hace un commit nuevo con el nuevo merge.
### Comandos
```git merge NOMBRE-DE-LA-RAMA```

Si hay algún cambio al que no se le ha hecho commit en la rama actual, Git no te permitirá fusionar hasta que se hayan realizado commit todos los cambios en tu rama actual. 

### Para manejar esos cambios, puedes hacer lo siguiente:

1. Crear una nueva rama y realizar commit a los cambios
2. ```git checkout -b nombre-de-la-nueva-rama```
3. ```git add .```
4. ```git commit -m "<tu mensaje de commit>"```
5. Guardarlos en el stash
6. ```git stash``` : agregarlos al stash
7. ```git merge new-features```: fusionarlos
8. ```git stash pop```: obtén los cambios devuelta al árbol de trabajo (working tree)
9. Abandonar todos los cambios
10. ```git reset --hard```: Remueve todos los cambios pendientes


- [ referencia:
 (https://www.freecodecamp.org/espanol/news/la-guia-definitiva-para-git-merge-y-git-rebase/)]