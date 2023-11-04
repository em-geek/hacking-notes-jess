#  Mind your Ps and Qs

## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)

## Solución
```python
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/mindyourps]  
└─$ python3  
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux  
Type "help", "copyright", "credits" or "license" for more information.  
>>> from Crypto.Util.number import long_to_bytes  
>>> from Crypto.Util.number import inverse  
>>>    
>>> c = 843044897663847841476319711639772861390329326681532977209935413827620909782846667  
>>> e = 65537  
>>> p = 2159947535959146091116171018558446546179  
>>> q = 658558036833541874645521278345168572231473  
>>> n = p * q  
>>> n  
1422450808944701344261903748621562998784243662042303391362692043823716783771691667  
>>> tn = (p-1)*(q-1)  
>>> d = inverse(e, tn)  
>>> m = pow(c,d,n)  
>>> m  
13016382529449106065927291425342535437996222135352905256639555294957886055592061  
>>> long_to_bytes(m)  
b'picoCTF{sma11_N_n0_g0od_00264570}'  
>>>
```

## Notas adicionales


## Referencias