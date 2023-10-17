# Glory of the Graden

## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.

## Solución
```bash
                                                                                                                                                                      ┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents]  
└─$ wget https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg  
--2023-10-16 10:47:58--  https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg  
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8  
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.  
HTTP request sent, awaiting response... 200 OK  
Length: 2295192 (2.2M) [application/octet-stream]  
Saving to: ‘garden.jpg.2’  
  
garden.jpg.2                              100%[===================================================================================>]   2.19M   122KB/s    in 55s        
  
2023-10-16 10:49:06 (40.8 KB/s) - ‘garden.jpg.2’ saved [2295192/2295192]  
  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents]  
└─$ hexeditor garden.jpg
```

La bandera esta hasta el final de la imagen dentro del editor hexadecimal.
La bandera es: picoCTF{more_than_m33ts_the_3y3657BaB2C}

## Notas adicionales


## Referencias