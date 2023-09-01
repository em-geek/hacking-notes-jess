# Level 3 -> 4

## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit3
Password:   aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

```

## Solucion
```bash
bandit3@bandit:~$ pwd  
/home/bandit3  
bandit3@bandit:~$ ls  
inhere  
bandit3@bandit:~$ cd inhere/  
bandit3@bandit:~/inhere$ ls -a  
.  ..  .hidden  
bandit3@bandit:~/inhere$ cat .hidden  
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe  
bandit3@bandit:~/inhere$ exit  
logout  
Connection to bandit.labs.overthewire.org closed.
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|cat      |Muestra el contenido del archivo en una salida estandar|
|ls -a| Lista todos los archivos en la carpeta actual, incluyendo los ocultos|
|ls -l| Lista los archivos en formato largo|
|ls -la|Lista todos los archivos en formato largo|

## Referencias
