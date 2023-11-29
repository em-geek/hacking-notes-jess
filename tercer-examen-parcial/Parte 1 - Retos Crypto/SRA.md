# SRA

## Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check... Connect to the program on our server: `nc saturn.picoctf.net 51015` Download the program: [chal.py](https://artifacts.picoctf.net/c/295/chal.py)

## Solución
El codigo es:
```bash
┌──(kali㉿kali)-[~/Documents/SRA]
└─$ cat exp.py 
from pwn import *
import primefac
from itertools import combinations
from Crypto.Util.number import long_to_bytes

#function to generate all the sub lists
def sub_lists (l):
   # initializing empty list
    comb = []

    #Iterating till length of list
    for i in range(1,len(l)+1):
       # Generating sub list
        comb += [list(j) for j in combinations(l, i)]
   # Returning list
    return comb

def divisors(phi):
   print("Give me the divisors of ", phi-1)
  # this is dangerous, but I'm trusting me
   return(eval(input()))

#connect to the server
r = remote('saturn.picoctf.net', 62417)
#get ciphertext
r.recvuntil("anger =")
ciphertext=int(r.recvline())
#get d
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print("d=",d)
print(r.recvuntil("vainglory?"))
r.recvline()
#since d is e^-1 mod (p-1)*(q-1), d*e=k*(p-1)*(q-1)+1
#so (p-1)*(q-1)*k = d*e-1
factors=divisors(d*65537)
combos = sub_lists(factors)
primes = set()
#try all possible subsets of the list of factors as the factors of (p-1)
for l in combos:
   product = 1
  # multiply them together to get p-1
   for k in l:
      product = product * k
  # if the right length and adding 1 yields a prime, then maybe
   if product.bit_length()==128 and primefac.isprime(product+1):
      primes.add(product+1)
print(primes)
primelist = list(primes)
#try all possible prime pairs
for p in primelist:
   for q in primelist:
      n=p*q
     # decode with this possible n
      plain = pow(ciphertext,d,n)
      try:
         plaintext = long_to_bytes(plain)
        # see if it corresponds to text and if so, try it
         print(plaintext.decode())
         r.sendline(plaintext.decode())
         print(r.recvline())
         print(r.recvline())
         print(r.recvline())
      except:
         continue

```

Se hizo:
```bash
┌──(kali㉿kali)-[~/Documents/SRA]
└─$ python3 exp.py 
[*] Checking for new versions of pwntools
    To disable this functionality, set the contents of /home/kali/.cache/.pwntools-cache-3.11/update to 'never' (old way).
    Or add the following lines to ~/.pwn.conf or ~/.config/pwn.conf (or /etc/pwn.conf system-wide):
        [update]
        interval=never
[*] You have the latest version of Pwntools (4.11.1)
[+] Opening connection to saturn.picoctf.net on port 50349: Done
/home/kali/Documents/SRA/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/kali/Documents/SRA/exp.py:29: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 62148178666654644511283048985037082351767102453578703014752556527630013337458
d= 70371547172924391280296970434653481960485671772850220332620594902099224090173
/home/kali/Documents/SRA/exp.py:33: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  4611940087071945831336822551375885247244349470977284889938955928098876849197667900
[2, 2, 3, 3, 5, 5, 17, 59, 5399, 19031, 42013, 2779449269, 6302503223, 3044545681506573468899, 22191530762674255789657]
{339802193809421516703312307888107700051, 323053004387357505712789058563988234567, 176075479863368845081330841694398958451}
62ZIsNo8iPecaLr1
/home/kali/Documents/SRA/exp.py:61: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> 62ZIsNo8iPecaLr1\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_2b7ad1ae}\r\n'
62ZIsNo8iPecaLr1
[*] Closed connection to saturn.picoctf.net port 50349

```


## Notas adicionales


## Referencias