# Level 2 -> 3

## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit2
Password:   rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi 

```

## Solucion
```bash
bandit2@bandit:~$ pwd  
/home/bandit2  
bandit2@bandit:~$ ls  
spaces in this filename  
bandit2@bandit:~$ cat "spaces in this filename"  
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG  
bandit2@bandit:~$ cat spaces\ in\ this\ filename  
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG  
bandit2@bandit:~$
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|cat      |Muestra el contenido del archivo en una salida estandar|

Este problema sucede porque al un nombre con espacios el comando lo va a detectar como si estuvieramos agregando varios argumentos, afortunadamente para este problema existen multiples soluciones, se pueden usar comillas dobles o se puede usar una diagonal invertida detras de un espacio, o al final de cada palabra, aunque esto se ve mas claro en la solucion 


## Referencias
https://linuxhandbook.com/filename-spaces-linux/