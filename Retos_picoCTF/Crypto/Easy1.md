#  Easy1

## Objetivo
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.

## Solución

El texto estaba en Vigenere, la primer solucion es usar la tabla que nos proporciona, esta tiene X y Y, en Y se va a localizar la letra de la llave, y despues vamos a recorrer la letras horizontalmente hasta que nos topemos con la letra codificada, una vez hecho la letra que se marque en el eje X sera la solucion, asi sera letra por letra, la segunda solucion sera usar cyberchef

## Notas adicionales


## Referencias