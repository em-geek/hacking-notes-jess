# Obedient Cat

## Objetivo
This file has a flag in plain sight (aka "in-the-clear").
## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ wget https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag  
   
--2023-09-25 10:50:51--  https://mercury.picoctf.net/static/2d24d50b4ebed90c70457  
5627f1f57b2/flag  
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142  
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... co  
nnected.  
HTTP request sent, awaiting response... 200 OK  
Length: 34 [application/octet-stream]  
Saving to: ‘flag’  
  
flag                 100%[===================>]      34  --.-KB/s    in 0s         
  
2023-09-25 10:50:55 (8.64 MB/s) - ‘flag’ saved [34/34]  
  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ cat flag  
picoCTF{s4n1ty_v3r1f13d_f28ac910}
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| wget     | Sirve para descargar archivos desde la terminal          |




## Referencias