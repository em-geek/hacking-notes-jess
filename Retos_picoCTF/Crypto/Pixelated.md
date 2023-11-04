#  Pixelated

## Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled2.png)

## Solución
```
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/pixelated]  
└─$ convert scrambled1.png scrambled2.png -compose Add -composite todo.png
```

Al unir ambas imagen usando convert este nos dara la bandera:
![[todo.png]]