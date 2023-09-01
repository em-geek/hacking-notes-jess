# Level 5 -> 6

## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit5
Password:   lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

## Solucion
```bash
bandit5@bandit:~$ pwd  
/home/bandit5  
bandit5@bandit:~$ ls  
inhere  
bandit5@bandit:~$ cd inhere/  
bandit5@bandit:~/inhere$ ls  
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16  
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17  
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18  
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19  
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c  
./maybehere07/.file2  
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2  
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                                                                                  
                           bandit5@bandit:~/inhere$ exit  
logout  
Connection to bandit.labs.overthewire.org closed.
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|cat      |Muestra el contenido del archivo en una salida estandar|
|ls -la|Lista todos los archivos en formato largo|
|file| Determina que tipo de archivo es el que pasemos como argumento|
|find| Permite buscar archivos de manera jerarquica|
|find -readable| Permite buscar archivos que sean leible por el usuario|
|find -type| Permite buscar archivos del tipo que se haya especificado|
|find -size| Permite buscar archivos con cierto tamaño especificado|

## Referencias
