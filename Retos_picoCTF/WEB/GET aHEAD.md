# GET aHEAD

## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:15931/](http://mercury.picoctf.net:15931/)

## Solución
```bash
picoCTF{r3j3ct_th3_du4l1ty_82880908}
```
Para resolver este problema se accedió a la pagina proporcionada, se inspecciono la pagina y en el apartado de red (network) se analizo las peticiones que se iban lanzando al presionar los botones, una vez presionados, se escogió cualquiera de las dos y se cambio el método de envió (los métodos que se estaban usando eran GET y POST) por HEAD, el cual en la respuesta devolvía la bandera.



## Notas adicionales


## Referencias