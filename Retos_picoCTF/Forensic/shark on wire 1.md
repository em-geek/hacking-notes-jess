#  shark on wire 1

## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag..

## Solución
```bash
                                                                                                                                                               picoCTF{StaT31355_636f6e6e}
                                                                                                                                                                  ```

Para la resolucion de este problema se escaneo el archivo dado con wireshark, despues buscamos el primer UDP que apareciera y le dimos follow UPD STREAM para encontrar la contraseña

## Notas adicionales


## Referencias