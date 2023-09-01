# Level 7 -> 8

## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit7
Password:   z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S 
```

## Solucion
```bash
 bandit7@bandit:~$ pwd  
/home/bandit7  
bandit7@bandit:~$ ls  
data.txt  
bandit7@bandit:~$ grep millionth data.txt  
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|grep|busca patrones dentro de un conjunto de texto|

## Referencias
