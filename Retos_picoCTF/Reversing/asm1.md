
#  asm1

## Objetivo
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/b41e08fc19ceb9d0466ebd68d36c5630/test.S)

## Solución
```shell
Stack  
  
0000  
  
  
  
ebp    <- esp <- ebp  
ret    <- ebp + 0x4  
0x6fa  <- ebp + 0x8  
fffff  
  
  
Registers  
[ 0x6e8 ] eax  
  
asm1:  
       <+0>:   push   ebp       
       <+1>:   mov    ebp,esp  
       <+3>:   cmp    DWORD PTR [ebp+0x8],0x3a2      
       <+10>:  jg     0x512 <asm1+37>              <- Se esta comparando 0x6fa > 0x3a2 (Da True)  
       <+12>:  cmp    DWORD PTR [ebp+0x8],0x358  
       <+19>:  jne    0x50a <asm1+29>  
       <+21>:  mov    eax,DWORD PTR [ebp+0x8]  
       <+24>:  add    eax,0x12  
       <+27>:  jmp    0x529 <asm1+60>  
       <+29>:  mov    eax,DWORD PTR [ebp+0x8]  
       <+32>:  sub    eax,0x12  
       <+35>:  jmp    0x529 <asm1+60>  
       <+37>:  cmp    DWORD PTR [ebp+0x8],0x6fa      
       <+44>:  jne    0x523 <asm1+54>              <- Se esta comparando 0x6fa != 0x6fa (Da False)  
       <+46>:  mov    eax,DWORD PTR [ebp+0x8]      <- Se guarda en eax el valor de ebp+0x8 = 0x6fa  
       <+49>:  sub    eax,0x12                     <- A 0x6fa se le resta 0x12 = 0x6e8  
       <+52>:  jmp    0x529 <asm1+60>  
       <+54>:  mov    eax,DWORD PTR [ebp+0x8]  
       <+57>:  add    eax,0x12  
       <+60>:  pop    ebp  
       <+61>:  ret
```

El registro eax fue la bandera: 0x6e8
## Notas adicionales


## Referencias

https://youtu.be/Dy-gHlymkdo?si=UrM63sok41P7TmZd