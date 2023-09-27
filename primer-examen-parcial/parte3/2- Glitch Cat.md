# Glitch Cat

## Objetivo
Our flag printing service has started glitching! `$ nc saturn.picoctf.net 49700`
## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ nc saturn.picoctf.net 49700  
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba1]  
└─$ python    
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux  
Type "help", "copyright", "credits" or "license" for more information.  
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'  
'picoCTF{gl17ch_m3_n07_a4392d2e}'  
>>> exit()
```

## Notas adicionales





## Referencias