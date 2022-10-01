# Glitch Cat
## Objetivo  
Our flag printing service has started glitching! `$ nc saturn.picoctf.net 65353`
## Solución  
al abrir abrir ese puertpo nos da la banderqa pero nos la da en codigo ascii
podemos traducirlo normalmente o con el mismo python
```shell

┌──(kali㉿kali)-[~/Downloads]
└─$ nc saturn.picoctf.net 65353
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
                                                                                                
┌──(kali㉿kali)-[~/Downloads]
└─$ python          
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + ')
  File "<stdin>", line 1
    print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + ')
                                                                                                                                     ^
SyntaxError: unterminated string literal (detected at line 1)
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64))
picoCTF{gl17ch_m3_n07_9c42a45d
>>> 


```
picoCTF{gl17ch_m3_n07_9c42a45d}

## Referencias
- []()