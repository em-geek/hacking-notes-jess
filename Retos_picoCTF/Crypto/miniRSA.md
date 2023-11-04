#  miniRSA

## Objetivo
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/d21037ad23ed84cfff20a84768a0f2b2/ciphertext)? Something seems a bit small.

## Solución
```python
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ python3             
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux  
Type "help", "copyright", "credits" or "license" for more information.  
>>> from gmpy2 import *  
>>> from Crypto.Util.number import long_to_bytes  
>>>    
>>> gmpy2.get_context().precision=2048  
>>>    
>>> e = 3  
>>> c = 2205316413931134031074603746928247799030155221252519872650073010782049179  
856976080512716237308882294226369300412719995904064931819531456392957957122459640  
736424089744772221933500860936331459280832211445548332429338572369823704784625368  
933  
>>>    
>>> root, exact = iroot(c, e)  
>>> root  
mpz(13016382529449106065894479374027604750406953699090365388203708028670029596145  
277)  
>>>    
>>> print(long_to_bytes(root) )  
b'picoCTF{n33d_a_lArg3r_e_ccaa7776}'  
>>>
```

## Notas adicionales


## Referencias