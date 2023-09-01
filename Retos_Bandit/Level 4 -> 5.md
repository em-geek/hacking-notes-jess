# Level 4 -> 5

## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit4
Password:   2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

```

## Solucion
```bash
bandit4@bandit:~$ pwd  
/home/bandit4  
bandit4@bandit:~$ ls  
inhere  
bandit4@bandit:~$ cd inhere/  
bandit4@bandit:~/inhere$ ls -la  
total 48  
drwxr-xr-x 2 root    root    4096 Apr 23 18:04 .  
drwxr-xr-x 3 root    root    4096 Apr 23 18:04 ..  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file00  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file01  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file02  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file03  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file04  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file05  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file06  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file07  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file08  
-rw-r----- 1 bandit5 bandit4   33 Apr 23 18:04 -file09  
bandit4@bandit:~/inhere$ file ./-*  
./-file00: data  
./-file01: data  
./-file02: data  
./-file03: data  
./-file04: data  
./-file05: data  
./-file06: data  
./-file07: ASCII text  
./-file08: data  
./-file09: Non-ISO extended-ASCII text, with no line terminators  
bandit4@bandit:~/inhere$ cat ./-file07  
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR  
bandit4@bandit:~/inhere$ exit  
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

## Referencias
