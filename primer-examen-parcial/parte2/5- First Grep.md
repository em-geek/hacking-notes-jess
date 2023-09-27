# First Grep

## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución

```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file  
      
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ cat file|grep picoCTF  
picoCTF{grep_is_good_to_find_things_dba08a45}                                                                       
```

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| wget     | Sirve para descargar archivos desde la terminal          |



## Referencias