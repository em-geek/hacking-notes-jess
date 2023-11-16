
#  GDB Test Drive

## Objetivo
Can you get the flag? Download this [binary](https://artifacts.picoctf.net/c/87/gdbme). Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`



## Solución
```shell
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking/gdbtestdrive]  
└─$ gdb gdbme        
GNU gdb (Debian 13.2-1) 13.2  
Copyright (C) 2023 Free Software Foundation, Inc.  
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>  
This is free software: you are free to change and redistribute it.  
There is NO WARRANTY, to the extent permitted by law.  
Type "show copying" and "show warranty" for details.  
This GDB was configured as "x86_64-linux-gnu".  
Type "show configuration" for configuration details.  
For bug reporting instructions, please see:  
<https://www.gnu.org/software/gdb/bugs/>.  
Find the GDB manual and other documentation resources online at:  
   <http://www.gnu.org/software/gdb/documentation/>.  
  
For help, type "help".  
Type "apropos word" to search for commands related to "word"...  
Reading symbols from gdbme...  
(No debugging symbols found in gdbme)  
(gdb) layout asm  
Undefined command: "layout".  Try "help".  
(gdb) layout asm  
Undefined command: "layout".  Try "help".  
(gdb) break *(main+99)  
Breakpoint 1 at 0x132a  
(gdb) dissasemble main  
Undefined command: "dissasemble".  Try "help".  
(gdb) set disassembly-flavor intel  
(gdb) disassemble main  
Dump of assembler code for function main:  
  0x00000000000012c7 <+0>:     endbr64  
  0x00000000000012cb <+4>:     push   rbp  
  0x00000000000012cc <+5>:     mov    rbp,rsp  
  0x00000000000012cf <+8>:     sub    rsp,0x50  
  0x00000000000012d3 <+12>:    mov    DWORD PTR [rbp-0x44],edi  
  0x00000000000012d6 <+15>:    mov    QWORD PTR [rbp-0x50],rsi  
  0x00000000000012da <+19>:    mov    rax,QWORD PTR fs:0x28  
  0x00000000000012e3 <+28>:    mov    QWORD PTR [rbp-0x8],rax  
  0x00000000000012e7 <+32>:    xor    eax,eax  
  0x00000000000012e9 <+34>:    movabs rax,0x4c75257240343a41  
  0x00000000000012f3 <+44>:    movabs rdx,0x4362383846336235  
  0x00000000000012fd <+54>:    mov    QWORD PTR [rbp-0x30],rax  
  0x0000000000001301 <+58>:    mov    QWORD PTR [rbp-0x28],rdx  
  0x0000000000001305 <+62>:    movabs rax,0x6630624760433530  
  0x000000000000130f <+72>:    movabs rdx,0x4e67646635656666  
  0x0000000000001319 <+82>:    mov    QWORD PTR [rbp-0x20],rax  
  0x000000000000131d <+86>:    mov    QWORD PTR [rbp-0x18],rdx  
  0x0000000000001321 <+90>:    mov    BYTE PTR [rbp-0x10],0x0  
  0x0000000000001325 <+94>:    mov    edi,0x186a0  
  0x000000000000132a <+99>:    call   0x1110 <sleep@plt>  
  0x000000000000132f <+104>:   lea    rax,[rbp-0x30]  
  0x0000000000001333 <+108>:   mov    rsi,rax  
  0x0000000000001336 <+111>:   mov    edi,0x0  
  0x000000000000133b <+116>:   call   0x1209 <rotate_encrypt>  
  0x0000000000001340 <+121>:   mov    QWORD PTR [rbp-0x38],rax  
  0x0000000000001344 <+125>:   mov    rdx,QWORD PTR [rip+0x2cc5]        # 0x4010 <stdout@@GLIBC_2.2.5>  
  0x000000000000134b <+132>:   mov    rax,QWORD PTR [rbp-0x38]  
  0x000000000000134f <+136>:   mov    rsi,rdx  
  0x0000000000001352 <+139>:   mov    rdi,rax  
  0x0000000000001355 <+142>:   call   0x10f0 <fputs@plt>  
  0x000000000000135a <+147>:   mov    edi,0xa  
  0x000000000000135f <+152>:   call   0x10c0 <putchar@plt>  
  0x0000000000001364 <+157>:   mov    rax,QWORD PTR [rbp-0x38]  
  0x0000000000001368 <+161>:   mov    rdi,rax  
--Type <RET> for more, q to quit, c to continue without paging--q  
Quit  
(gdb) run  
Starting program: /home/emgeek/Documents/pruebasHacking/gdbtestdrive/gdbme    
[Thread debugging using libthread_db enabled]  
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".  
  
Breakpoint 1, 0x000055555555532a in main ()  
(gdb) jump *(main+104)  
Continuing at 0x55555555532f.  
picoCTF{d3bugg3r_dr1v3_7776d758}  
[Inferior 1 (process 3737) exited normally]  
(gdb)
```


## Notas adicionales


## Referencias