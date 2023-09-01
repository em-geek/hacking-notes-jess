# Level 8 -> 9

## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit8
Password:   TESKZC0XvTetK0S9xNwm25STk5iWrBvP 
```

## Solucion
```bash
bandit8@bandit:~$ pwd  
/home/bandit8  
bandit8@bandit:~$ ls  
data.txt  
bandit8@bandit:~$ cat    
.bash_logout  .bashrc       data.txt      .profile         
bandit8@bandit:~$ cat data.txt | sort | uniq -u  
EN632PlfYiZbn3PhVK3XOGSlNInNE00t  
bandit8@bandit:~$
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|sort|ordena un conjunto de datos|
|uniq|filtra los datos pasados segun las necesidades del usuario|
|uniq -u|Muestra los datos que no se repiten|

## Referencias
