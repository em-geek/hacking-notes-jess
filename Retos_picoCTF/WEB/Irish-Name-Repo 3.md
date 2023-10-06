# Irish-Name-Repo 3

## Objetivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!
## Solución
```bash
password: ' BE 4==4;
SQL query: SELECT * FROM admin where password = '' OR 4==4;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}
```

Se utilizo inyeccion SQL, se entro al login de la pagina, para despues inspeccionar la pagina y despues hacer que el cuadro de texto debug ahora sea visible, una vez hecho esto en el apartado de username se escribio: admin';
Una vez escrito eso, un password cualquiera y en el recuadro de debug escribir 1, la pagina lanza la bandera. Esta vez al escribir cualquier cosa el texto se le aplicaba un rot13, por lo que ahora la inyeccion se le aplico un rot13, de modo que cuando el login le aplique de nuevo un rot13, el codigo se va a inyectar

## Notas adicionales


## Referencias