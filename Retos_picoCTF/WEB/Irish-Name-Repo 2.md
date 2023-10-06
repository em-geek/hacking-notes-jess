# Irish-Name-Repo 2

## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649
## Solución
```bash
username: admin';
password: hola
SQL query: SELECT * FROM users WHERE name='admin';' AND password='hola'

# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_aee925db}
```

Se utilizo inyeccion SQL, se entro al login de la pagina, para despues inspeccionar la pagina y despues hacer que el cuadro de texto debug ahora sea visible, una vez hecho esto en el apartado de username se escribio: admin';
Una vez escrito eso, un password cualquiera y en el recuadro de debug escribir 1, la pagina lanza la bandera. Esta vez al inyectar eso la cadena SQL que se esta mandando en cuanto lee el punto y coma ya no valida el password

## Notas adicionales


## Referencias