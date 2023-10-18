#  shark on wire 2

## Objetivo
	We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Solución
```bash
                                                                                                                                                               >>> chr(112) + chr(105) + chr(99) + chr(111) + chr(67) + chr(84) + chr(70) + chr(  
123) + chr(112) + chr(49) + chr(76) + chr(76) + chr(102) + chr(51) + chr(114) + c  
hr(51) + chr(100) + chr(95) + chr(100) + chr(97) + chr(116) + chr(97) + chr(95) +  
chr(118) + chr(49) + chr(97) + chr(95) + chr(115) + chr(116) + chr(51) + chr(103  
) + chr(48) + chr(125)  
'picoCTF{p1LLf3r3d_data_v1a_st3g0}'
                                                                                                                                                                  ```

Para la resolucion de este problema se escaneo el archivo dado con wireshark, despues buscamos el primer UDP, despues de revisarlos notamos una anomalia, y es que en los UDP que se mandan al puerto 22 el primero comienza con la palabra START y el segundo con END, por lo que se revisaron los paquetes y despues de verlos se encontro que en en los puertos source estaba escrito la bandera

## Notas adicionales


## Referencias