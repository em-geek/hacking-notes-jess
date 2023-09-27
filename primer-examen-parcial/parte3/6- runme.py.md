# runme.py

## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución
```bash
                                                                                  ┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ wget https://artifacts.picoctf.net/c/34/runme.py          
--2023-09-27 12:41:44--  https://artifacts.picoctf.net/c/34/runme.py  
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55  
.64, 3.161.55.26, ...  
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443...  
connected.  
HTTP request sent, awaiting response... 200 OK  
Length: 270 [application/octet-stream]  
Saving to: ‘runme.py’  
  
runme.py             100%[===================>]     270  --.-KB/s    in 0s         
  
2023-09-27 12:41:56 (51.9 MB/s) - ‘runme.py’ saved [270/270]  
  
                                                                                   
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/prueba2]  
└─$ python runme.py    
picoCTF{run_s4n1ty_run}
```

## Notas adicionales





## Referencias