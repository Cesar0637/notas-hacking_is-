# unpackme.py
## Objetivo
Can you get the flag? Reverse engineer this [Python program](https://artifacts.picoctf.net/c/466/unpackme.flag.py).

## Soluciòn
solamente hay que agregar un print al plain para imprimir el funcionamiento
```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ nano unpackme.flag.py

┌──(kali㉿kali)-[~/Downloads]
└─$ cat unpackme.flag.py   
import base64
from cryptography.fernet import Fernet



payload = b'gAAAAABiMD09KmaS5E6AQNpRx1_qoXOBFpSny3kyhr8Dk_IEUu61Iu0TaSIf8RCyf1LJhKUFVKmOt2hfZzynRbZ_fSYYN_OLHTTIRZOJ6tedEaK6UlMSkYJhRjAU4PfeETD-8gDOA6DQ8eZrr47HJC-kbyi3Q5o3Ba28mutKCAkwrqt3gYOY9wp3dWYSWzP4Tc3NOYWfu-SJbW997AM8GA-APpGfFrf9f7h0VYcdKOKu4Vq9zjJwmTG2VXWFET-pkF5IxV3ZKhz36L5IvZy1dVZXqaMR96lovw=='

key_str = 'correctstaplecorrectstaplecorrec'
key_base64 = base64.b64encode(key_str.encode())
f = Fernet(key_base64)
plain = f.decrypt(payload)
print(plain.decode())
exec(plain.decode())

┌──(kali㉿kali)-[~/Downloads]
└─$ python  unpackme.flag.py             

pw = input('What\'s the password? ')

if pw == 'batteryhorse':
  print('picoCTF{175_chr157m45_5274ff21}')
else:
  print('That password is incorrect.')


What's the password? 


```
picoCTF{175_chr157m45_5274ff21}

## Referencias
- []()