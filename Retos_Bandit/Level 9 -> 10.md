# Level 9 -> 10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit9
Password:   EN632PlfYiZbn3PhVK3XOGSlNInNE00t 
```

## Solucion
```bash
bandit9@bandit:~$ pwd  
/home/bandit9  
bandit9@bandit:~$ ls  
data.txt  
bandit9@bandit:~$ strings data.txt | grep ====  
4========== the#  
========== password  
========== is  
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s  
bandit9@bandit:~$
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|grep|busca patrones dentro de un conjunto de texto|
|strings|muestra el texto legible dentro de un archivo|

## Referencias
