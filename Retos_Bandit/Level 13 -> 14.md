# Level 13 -> 14

## Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit13
Password:   wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

## Solucion
```bash
bandit13@bandit:~$ pwd  
/home/bandit13  
bandit13@bandit:~$ ls  
sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220  
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be establish  
ed.  
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.  
This key is not known by any other names  
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes  
Could not create directory '/home/bandit13/.ssh' (Permission denied).  
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_host  
s).
..
..
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14  
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq  
bandit14@bandit:~$ exit  
logout  
Connection to localhost closed.  
bandit13@bandit:~$ exit  
logout  
Connection to bandit.labs.overthewire.org closed.
```


## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|ssh|Nos permite conectarnos de manera remota a otro ordenador|
|cat|Concatena archivos en una salida estandar|

## Referencias
