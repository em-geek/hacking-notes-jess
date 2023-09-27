### Nice Netcat

## Objetivo
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22342`, but it doesn't speak English...
## Solución
```bash
┌──(emgeek㉿EmGeek-Kali-PC)-[~]  
└─$ nc mercury.picoctf.net 22342  
112    
105    
99    
111    
67    
84    
70    
123    
103    
48    
48    
100    
95    
107    
49    
116    
116    
121    
33    
95    
110    
49    
99    
51    
95    
107    
49    
116    
116    
121    
33    
95    
53    
102    
98    
53    
101    
53    
49    
100    
125    
10
```

Esos numeros los transforme de decimales a ascii, usando una pagina de internet, esta me dio como resultado: picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}

## Notas adicionales
La pagina usada es https://onlinetools.com/ascii/convert-decimal-to-ascii




## Referencias