# miniRSA
## Objetivo
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/ee7e2388b45f521b285334abb5a63771/ciphertext)? Something seems a bit small.

## Soluciòn

formulario
```text
c - texto cifrado
m - mensajo en texto plano (lo que se va encriptar)
p - primo 1
q - primo 2
n - modulo
tn - totient n (euler)
e - exponente (llave publica, suele ser 216 + 1=65537 )
d - llave privada

n = p * q
tn = (p-1)*(q-1)
d = e mod inv tn / python -> inverse(e,tn)

Encriptar c = m^e mod n / python -> pow(m,e,n)

Desencriptar m = c^d mod n / python -> pow(c,d,n)
```

en python importamos estas librerias y utilizamos la formula
```python
>>> from gmpy2 import *
>>> from Crypto.Util.number import long_to_bytes
>>> c =2205316413931134031074603746928247799030155221252519872650080519263755075355825243327515211479747536697517688468095325517209911688684309894900992899707504087647575997847717180766377832435022794675332132906451858990782325436498952049751141 
>>> e=3
>>> root, exact=iroot(c,e)
>>> root                                                                                                                                                               
mpz(13016382529449106065894479374027604750406953699090365388203722801043052339225981)
>>> print(long_to_bytes(root))    b'picoCTF{n33d_a_lArg3r_e_d0cd6eae}'

```


picoCTF{n33d_a_lArg3r_e_d0cd6eae}
## Referencias
- []()