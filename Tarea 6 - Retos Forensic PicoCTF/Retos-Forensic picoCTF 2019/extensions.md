# extensions
## Objetivo
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?

## Soluciòn
usando el comando file vemos que en realidad es una imagen 
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ file flag.txt
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
                                                                         
                                         
┌──(kali㉿kali)-[~/Downloads]
└─$ mv flag.txt flag.png
                                                                         
┌──(kali㉿kali)-[~/Downloads]

└─$ open flag.png
                                                                         

```
lo que nos da es una imagen con la bandera

picoCTF{now_you_know_about_extensions}

## Referencias
- []()