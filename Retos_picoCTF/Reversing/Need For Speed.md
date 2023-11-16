
#  Need For Speed

## Objetivo
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/cd51b2c95be9f3626db6fe6665afb5a3/need-for-speed).

## Solución
```shell
(gdb) break main  
Breakpoint 1 at 0x55555540091e  
(gdb) run  
Starting program: /home/emgeek/Documents/pruebasHacking/needforspeed/need-for-speed    
[Thread debugging using libthread_db enabled]  
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".  
  
Breakpoint 1, 0x000055555540091e in main ()  
(gdb) call (int) header()  
Keep this thing over 50 mph!  
============================  
  
$1 = 2  
(gdb) call (int) get_key()  
Creating key...  
Finished  
$2 = 9  
(gdb) call (int) print_flag()  
Printing flag:  
PICOCTF{Good job keeping bus #24c43740 speeding along!}  
$3 = 56  
(gdb)
```


## Notas adicionales


## Referencias