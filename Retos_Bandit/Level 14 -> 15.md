# Level 14 -> 15

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit14
Password:   fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```

## Solucion
```bash
bandit14@bandit:~$ ls  
bandit14@bandit:~$ pwd  
/home/bandit14  
bandit14@bandit:~$ man nc  
bandit14@bandit:~$ nc localhost 30000  
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq  
Correct!  
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt  
  
^Z  
[1]+  Stopped                 nc localhost 30000  
bandit14@bandit:~$ exit  
logout  
There are stopped jobs.
```


## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|nc (netcat)|Este comando envuelve todo lo que tenga que ver con TCP, UDP o sockets|

Para mejor comprension este comando lo que esta haciendo es abrir un socket para mandar y enviar mensajes, en este ejercicio el puerto 30000 esta escuchando esperando la contraseña del reto bandit14, por lo que al mandarle al puerto la contraseña este respondera con la contraseña del reto bandit15.
Despues de documentar note que no cerre el socket, solo me sali a la fuerza, para cerrarlo es usar CTRL + C.
## Referencias
