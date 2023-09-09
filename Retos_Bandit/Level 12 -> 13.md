# Level 12 -> 13

## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de Acceso al nivel
```
Server:     bandit.labs.overthewire.org
User:       bandit12
Password:   JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```

## Solucion
```bash
bandit12@bandit:~$ xxd -r data.txt | file -  
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023,  
max compression, from Unix  
bandit12@bandit:~$ xxd -r data.txt | zcat | file -  
/dev/stdin: bzip2 compressed data, block size = 900k  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | file -  
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023,  
max compression, from Unix  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | file -  
/dev/stdin: POSIX tar archive (GNU)  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar x0 | file -  
tar: Options '-[0-7][lmh]' not supported by *this* tar  
Try 'tar --help' or 'tar --usage' for more information.  
/dev/stdin: empty  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -  
/dev/stdin: POSIX tar archive (GNU)  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -  
/dev/stdin: bzip2 compressed data, block size = 900k  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | file -  
/dev/stdin: POSIX tar archive (GNU)  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO  
| file -  
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023,  
max compression, from Unix  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO  
| zcat | file -  
/dev/stdin: ASCII text  
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO  
| zcat    
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw  
bandit12@bandit:~$
```


## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |         
| ls      | Lista los archivos en la carpeta actual |
|xxd | Crea un vaciado hexadecimal de un archivo dado |
|xxd -r | Conviete un vaciado hexadecimal a binario |
|zcat | Sirve para descomprimir archvivos de tipo gzip |
|bzcat | Sirve para descomprimir archvivos de tipo bzip |
|tar |Sirve para comprimir uno o mas archivos |
|file |Sirve para determinar el tipo de archivo|

## Referencias
