# Secrets 

## Objetivo
We have several pages hidden. Can you find the one with the flag? The website is running [here](http://saturn.picoctf.net:65455/).

## Solución
Se inspecciono la pagina dada por el reto, dentro de esta pagina existe el index ubicado en view-source:http://saturn.picoctf.net:65455/secret/assets/index.css, por lo cual al ver que dice secret escribi en el navegador view-source:http://saturn.picoctf.net:65455/secret/, la cual muestra:

```html
<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <link rel="stylesheet" href="[hidden/file.css](view-source:http://saturn.picoctf.net:65455/secret/hidden/file.css)" />
  </head>

  <body>
    <h1>Finally. You almost found me. you are doing well</h1>
    <img src="[https://media1.tenor.com/images/0a6aff9f825af62c05adfbd75039cc7b/tenor.gif?itemid=4648337](view-source:https://media1.tenor.com/images/0a6aff9f825af62c05adfbd75039cc7b/tenor.gif?itemid=4648337)" alt="Something Like That GIF - Andy Parksandrecreation Wtf GIFs" style="max-width: 833px; background-color: rgb(151, 121, 85);" width="833" height="937.125">
  </body>
</html>
```

Hay otra pagina que ahora tiene la palabra hidden, por lo tanto ahora vamos a hacer lo mismo, estando ahi, nos dara otra direccion, al entrar a esa direccion nos dara la pagina la bandera: picoCTF{succ3ss_@h3n1c@10n_39849bcf}