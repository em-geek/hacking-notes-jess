Documento con paginas y programas

## Paginas

- https://gchq.github.io/CyberChef/
- https://onlinetools.com/ascii/convert-decimal-to-ascii
- https://playcode.io/javascript

## Programas
- https://obsidian.md/

## Formulas RSA

c = texto cifrado
m = mensaje texto plano
p = primo 1
q = primo 2
n = modulo
tn = totient n (euler)
e = exponente (llave publica) 2^16+1 = 65537

n = p * q
tn = (p-1) * (q-1)
d = e mod inv tn  /  inverse(e, tn)

Encriptar          : c = m^e mod n    /  pow(m,e,n)

Desencriptar   : c = c^d  mod n    /  pow(c,d,n) 
