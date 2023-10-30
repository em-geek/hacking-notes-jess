#  WebNet1

## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/webnet1]  
└─$ strings vulture.jpg | grep picoCTF  
picoCTF{honey.roasted.peanuts}
																																								  ```
Para la resolucion de este problema se escaneo el archivo dado con wireshark, despues de revisarlo un poc  se noto que los datos estaban encriptados, afortunadamente se tenia la llave privada, se fue a preferencias y en el protocolo TLS se agrego la llave, los archivos HTTP ahora desencriptado podian leerse, por lo cual se extrajeron los datos que se mandaron por HTTP, ahi venia una imagen, y al aplicarle strings a la imagen se encontro la bandera
	
## Notas adicionales


## Referencias