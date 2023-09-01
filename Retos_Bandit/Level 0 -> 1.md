# Level 0 -> 1

## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit0
Password:   bandit0

```

## Solucion
```bash
bandit0@bandit:~$ ls  
readme  
bandit0@bandit:~$ cat readme    
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|cat      |Muestra el contenido del archivo en una salida estandar|




## Referencias

