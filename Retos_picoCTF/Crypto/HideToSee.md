#  HideToSee

## Objetivo
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/240/atbash.jpg).

## Solución

```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/hidetosee]  
└─$ steghide --extract -sf atbash.jpg  
Enter passphrase:    
wrote extracted data to "encrypted.txt".  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/hidetosee]  
└─$ ls      
atbash.jpg  encrypted.txt  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/hidetosee]  
└─$ cat encrypted.txt    
krxlXGU{zgyzhs_xizxp_xz00558y}  
                                                                                                                                                             
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/hidetosee]  
└─$ echo picoCTF{atbash_crack_ca00558b}     
picoCTF{atbash_crack_ca00558b}
```

## Notas adicionales


## Referencias