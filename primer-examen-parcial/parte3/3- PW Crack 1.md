# PW Crack 1

## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Solución
```bash
                                                                                 ┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ wget https://artifacts.picoctf.net/c/12/level1.py  

┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc  

┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ python level1.py                        
Please enter correct password for flag: hello  
That password is incorrect  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ nano level1.flag.txt.enc    
  
  
Use "fg" to return to nano.  
zsh: suspended (signal)  nano level1.flag.txt.enc  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ strings level1.flag.txt.enc    
H^R\{cwH  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ nano level1.py             
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ python level1.py                                              
Please enter correct password for flag: 8713  
Welcome back... your flag, user:  
picoCTF{545h_r1ng1ng_1b2fd683}
```

## Notas adicionales





## Referencias