# Tags
- Son una referencia a un commit especifico para dejar un registro historico como versiones de un programa.

### jerarquia numeros versiones
- 1: cambios importantes en la aplicacion
- 1.0: cambios en funcionalidades o nuevas funcionalidades
- 1.0.0: correccion de errores
  

### comandos y argumentos
-m: mensaje
-a: version del tag
-d: Eliminar tag
-show: Muestra el detalle de un tag

1. crear tag: ```git tag -a v1.0.0  -m “version 1.0.0 done”```
2. eliminar : ```git tag -d nombreTag```
3. Agregar un commit anterior a un tag, solo se debe copiar el hash(id) del commit y ejecutar: ```git tag -a v0.1.0 hasgCommit -m “version alfa de blabla”```
1. ver mas info de un tag: ```git show v1.0.0 ```( o la version que se quiere ver)


