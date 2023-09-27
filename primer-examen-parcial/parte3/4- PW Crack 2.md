# PW Crack 2

## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución
```bash
                                                                                 ┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ wget https://artifacts.picoctf.net/c/14/level2.py             

┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc  

┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ ls  
level2.flag.txt.enc  level2.py  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ python level2.py  
Please enter correct password for flag: 1234  
That password is incorrect  
                                                                         
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ nano level2.py    

┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ python              
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux  
Type "help", "copyright", "credits" or "license" for more information.  
>>> 'user_pw ==' +  chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)  
'user_pw ==4ec9'  
>>> exit()  

┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ python level2.py  
Please enter correct password for flag: 4ec9  
Welcome back... your flag, user:  
picoCTF{tr45h_51ng1ng_9701e681}
```

## Notas adicionales





## Referencias