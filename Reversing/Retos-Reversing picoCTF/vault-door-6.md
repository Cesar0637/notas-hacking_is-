# vault-door-6
## Objetivo
This vault uses an XOR encryption scheme. The source code for this vault is here: [VaultDoor6.java](https://jupiter.challenges.picoctf.org/static/937a166e2c8c5bf34928a2dab22e8ade/VaultDoor6.java)

## Soluciòn
al observar el codigo que descargamos obserrvamos algo similar al anterior, lo mas probable esque la bandera este en myBytes tambien
primero lo convertimos a caracteres con python 
ejecutamos los siguientes comandos
```python
myBytes =[0x3b,0x65,0x21,0xa,0x38,0x0,0x36,0x1d,0xa,0x3d,0x61,0x27,0x11,0x66,0x27,0xa,0x21,0x1d,0x61,0x3b,0xa,0x2d,0x65,0x27,0xa,0x66,0x36,0x30,0x67,0x6c,0x64,0x6c]
myBytes 

```
myBytes
[59, 101, 33, 10, 56, 0, 54, 29, 10, 61, 97, 39, 17, 102, 39, 10, 33, 29, 97, 59, 10, 45, 101, 39, 10, 102, 54, 48, 103, 108, 100, 108]
ahora aplicamos el siguiente comando
```python

>>> bandera=[i ^ 0x55 for i in myBytes]
>>> bandera
[110, 48, 116, 95, 109, 85, 99, 72, 95, 104, 52, 114, 68, 51, 114, 95, 116, 72, 52, 110, 95, 120, 48, 114, 95, 51, 99, 101, 50, 57, 49, 57]

Por ultimo lo convertimos a letra y ya 

>>> bandera=[chr(i) for i in bandera]
>>> bandera
['n', '0', 't', '_', 'm', 'U', 'c', 'H', '_', 'h', '4', 'r', 'D', '3', 'r', '_', 't', 'H', '4', 'n', '_', 'x', '0', 'r', '_', '3', 'c', 'e', '2', '9', '1', '9']

>>> ''.join(bandera)
'n0t_mUcH_h4rD3r_tH4n_x0r_3ce2919' 
```
picoCTF{n0t_mUcH_h4rD3r_tH4n_x0r_3ce2919}

## Referencias
- []()