### Wave a flag

## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...
## Solución
```bash
                                                                                 ┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm  
   
--2023-09-25 10:56:04--  https://mercury.picoctf.net/static/b28b6021d6040b086c222  
6ebeb913bc2/warm  
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142  
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... co  
nnected.  
HTTP request sent, awaiting response... 200 OK  
Length: 10936 (11K) [application/octet-stream]  
Saving to: ‘warm’  
  
warm                 100%[===================>]  10.68K  --.-KB/s    in 0s         
  
2023-09-25 10:56:12 (39.0 MB/s) - ‘warm’ saved [10936/10936]  
  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ ls  
Desktop    Downloads  Pictures  Templates  flag  
Documents  Music      Public    Videos     warm  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ ./warm           
zsh: permission denied: ./warm  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ chmod +x warm  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ ./warm          
Hello user! Pass me a -h to learn what I can do!  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ ./warm -h  
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| wget     | Sirve para descargar archivos desde la terminal          |
| chmod +x     | Da permisos de ejecucion          |




## Referencias