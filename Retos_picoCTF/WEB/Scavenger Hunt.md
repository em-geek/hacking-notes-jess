# Scavenger Hunt

## Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:27393/](http://mercury.picoctf.net:27393/). Can you find it?

## Solución
```bash
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_d375c750}
```
Las partes se estuvieron buscando en diferentes sitios de la pagina inspeccionando la pagina principal y moviéndose a diferentes partes, ya sea su html, css, js, robots:
Parte 1: view-source:http://mercury.picoctf.net:27393/ (`picoCTF{t`)
Parte 2: view-source:http://mercury.picoctf.net:27393/mycss.css (`h4ts_4_l0`)
Parte 3: http://mercury.picoctf.net:27393/robots.txt (`t_0f_pl4c`)
Parte 4: http://mercury.picoctf.net:27393/.htaccess (`3s_2_lO0k`)
Parte 5: http://mercury.picoctf.net:27393/.DS_Store (`_d375c750}`)

Cuando se escaneo el js este decía que que como evitábamos que Google indexe nuestro sitio, esto se hace dentro del archivo robots.txt, entonces, ahí estaba la 3er parte de la bandera.
Donde se encontraba la tercera parte de la bandera, había una pista que decía que la pagina estaba montada en apache, por lo cual inmediatamente se trato acceder a .htaccess, lo cual fue satisfactorio, encontrando la cuarta parte de la bandera.
Por ultimo la quinta bandera esta en el archivo .DS_Store, este se encontró gracias a la pista donde se encontró la cuarta, esta pista dice que el usuario ama crear websites en Mac, la mac crea el archivo .DS_Store, por lo cual la pagina al no tener los permisos adecuados ni los cuidados este archivo también es accesible


## Notas adicionales


## Referencias