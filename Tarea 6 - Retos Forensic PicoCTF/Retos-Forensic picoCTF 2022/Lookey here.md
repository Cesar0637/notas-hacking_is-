#  Lookey here
## Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/296/anthem.flag.txt).

## Soluciòn
primero vemos de que tipo es el archivo para saber como tratarlo 
```shell
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ file anthem.flag.txt 
anthem.flag.txt: Unicode text, UTF-8 text
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ cat anthem.flag.txt | grep "picoCTF"   
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}

```
picoCTF{gr3p_15_@w3s0m3_4c479940}

## Referencias
- []()