# fixme2.py

## Objetivo
Fix the syntax error in the Python script to print the flag.
## Solución
```bash
┌┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ wget https://artifacts.picoctf.net/c/6/fixme2.py                     
                                                                               
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ python fixme2.py    
 File "/home/emgeek/Documents/prueba1/fixme2.py", line 22  
   if flag = "":  
      ^^^^^^^^^  
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ nano fixme2.py    
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ python fixme2.py  
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| wget     | Sirve para descargar archivos desde la terminal          |




## Referencias