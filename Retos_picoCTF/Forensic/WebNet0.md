#  WebNet0

## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/webnet0]  
└─$ sudo ssldump -r capture.pcap -k picopico.key -d | grep picoCTF -A 2 -B 2  
   0a 43 6f 6e 74 65 6e 74 2d 45 6e 63 6f 64 69 6e    .Content-Encodin  
   67 3a 20 67 7a 69 70 0d 0a 50 69 63 6f 2d 46 6c    g: gzip..Pico-Fl  
   61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong  
   73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac  
   6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L  
--  
   43 6f 6e 74 65 6e 74 2d 45 6e 63 6f 64 69 6e 67    Content-Encoding  
   3a 20 67 7a 69 70 0d 0a 50 69 63 6f 2d 46 6c 61    : gzip..Pico-Fla  
   67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs  
   68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack  
   65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le   
																																								  ```

Para la resolucion de este problema se escaneo el archivo dado con wireshark, despues de revisarlo un poc  se noto que los datos estaban encriptados, afortunadamente se tenia la llave privada, se fue a preferencias y en el protocolo TLS se agrego la llave, los archivos HTTP ahora desencriptado podian leerse, por lo cual con la herramienta de buscar se localizo la bandera, la cual fue picoCTF{nongshim.shrimp.crackers}

Como alternativa tambien se muestra la solucion usando la terminal
## Notas adicionales


## Referencias