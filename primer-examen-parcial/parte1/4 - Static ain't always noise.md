### Static ain't always noise
## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static)?
## Solución
```bash
                                                                                 ┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/stat  
ic  

┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ chmod +x static    
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ ./static    
Oh hai! Wait what? A flag? Yes, it's around here somewhere!  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ strings static | grep pico  
picoCTF{d15a5m_t34s3r_98d35619}
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| wget     | Sirve para descargar archivos desde la terminal          |
| chmod +x     | Da permisos de ejecucion          |




## Referencias