
#  asm2

## Objetivo
What does asm2(0x4,0x21) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/7e3eb2f90200ac88126f62ceb4bc3948/test.S)

## Solución
```shell
 GNU nano 7.2                                       test.S *                                                  
Pila  
  
---- <- esp  
----  
0x78  
0x22 <- ebp - 0x4  
ebp <-ebp  
ret <- ebp + 0x4  
0x4 <- ebp + 0x8  
0x21  
  
registros      
0x24c   <- eax  
  
asm2:  (0x4, 0x21)  
       <+0>:   push   ebp       
       <+1>:   mov    ebp,esp    
       <+3>:   sub    esp,0x10  
       <+6>:   mov    eax,DWORD PTR [ebp+0xc]  
       <+9>:   mov    DWORD PTR [ebp-0x4],eax  
       <+12>:  mov    eax,DWORD PTR [ebp+0x8]  
       <+15>:  mov    DWORD PTR [ebp-0x8],eax  
       <+18>:  jmp    0x509 <asm2+28>  
       <+20>:  add    DWORD PTR [ebp-0x4],0x1    --Suma 0x1 a ebp-0x4  
       <+24>:  add    DWORD PTR [ebp-0x8],0x74  
       <+28>:  cmp    DWORD PTR [ebp-0x8],0xfb46 --Comparacion menor o igual (Esta comparacion dara 555 vu>  
       <+35>:  jle    0x501 <asm2+20>            --Si la comparacion es verdadera salta a la linea 20  
       <+37>:  mov    eax,DWORD PTR [ebp-0x4]  
       <+40>:  leave     
       <+41>:  ret
```

El registro eax fue la bandera: 0x24c
## Notas adicionales


## Referencias

https://youtu.be/R4r1cbBvPqk?si=k_BY1S623fi_duQx