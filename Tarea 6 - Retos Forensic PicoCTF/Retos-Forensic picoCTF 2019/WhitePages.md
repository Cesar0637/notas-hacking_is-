# WhitePages

## Objetivo


## Soluciòn
creamos el siguiente script de python y lo corremos 
```python 
from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)

print(data)
```


```shell

┌──(kali㉿kali)-[~/Downloads]
└─$ nano exp.py                
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python exp.py 
b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}\n\t\t'
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python exp.py

```
picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}

## Referencias