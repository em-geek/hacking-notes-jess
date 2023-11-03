# Lookey here

## Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/124/anthem.flag.txt).

## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/lookey]  
└─$ wget https://artifacts.picoctf.net/c/124/anthem.flag.txt    
--2023-10-31 23:45:28--  https://artifacts.picoctf.net/c/124/anthem.flag.txt  
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.124.119, 18.160.124.34, 18.160.124.108, ...  
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.124.119|:443... connected.  
HTTP request sent, awaiting response... 200 OK  
Length: 108668 (106K) [application/octet-stream]  
Saving to: ‘anthem.flag.txt’  
  
anthem.flag.txt                           100%[===================================================================================>] 106.12K   508KB/s    in 0.2s       
  
2023-10-31 23:45:29 (508 KB/s) - ‘anthem.flag.txt’ saved [108668/108668]  
  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/lookey]  
└─$ cat anthem.flag.txt | grep pico    
     we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}  
                                                                                                                                                                        
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/lookey]  
└─$
```