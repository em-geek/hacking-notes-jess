# Level 1 -> 2

## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit1
Password:   NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

```

## Solucion
```bash
bandit1@bandit:~$ ls  
-  
bandit1@bandit:~$ cat ./-  
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi  
bandit1@bandit:~$
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|cat      |Muestra el contenido del archivo en una salida estandar|

Este problema sucede porque al poner ''-'' el comando cat estara esperando el comando especifico, asi que para archivos con nombres con caracteres especiales se necesita especificar la ruta completa, o bien, en mi caso lo hice indicando la ruta actual y listo


## Referencias
https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal
