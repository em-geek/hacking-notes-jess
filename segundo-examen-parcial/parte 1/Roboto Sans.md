# Roboto Sans

## Objetivo
The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:59901/) out.

## Solución
El nombre del reto me dio la idea de revisar el robots.txt, por lo que ahi recibi el mensaje: Think you have seen your flag or want to keep looking. La pagina de robots es la siguiente:
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```

Si somos observadores aparece el texto: anMvbXlmaWxlLnR4dA== ,  el cual esta en base64, traducido dice: js/myfile.txt, si accedemos a esa direccion obtendremos la direccion: picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}