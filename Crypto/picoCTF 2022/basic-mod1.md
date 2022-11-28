# basic-mod1
## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/394/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Soluciòn
```shell     
┌──(kali㉿kali)-[~/Downloads]
└─$ cat message.txt 
54 396 131 198 225 258 87 258 128 211 57 235 114 258 144 220 39 175 330 338 297 288                                                                                  
┌──(kali㉿kali)-[~/Downloads]
└─$ nano scp.py                
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ python scp.py 
['54', '396', '131', '198', '225', '258', '87', '258', '128', '211', '57', '235', '114', '258', '144', '220', '39', '175', '330', '338', '297', '288']
picoCTF{R0UND_N_R0UND_79C18FB3}
                                   
```
scp.py
```python
datos=open('message.txt').read().split()

print(datos)

flag=''

for n in datos:
 c=int(n) % 37
 if c >= 0 and c <=  25:
  s=chr(c + 65)
 elif c >= 26 and c <= 35:
  s=chr(c + 22)
 else:
  s='_'
 flag+=s

print(f"picoCTF{{{flag}}}")

```

picoCTF{R0UND_N_R0UND_B6B25531}

## Referencias
- []()