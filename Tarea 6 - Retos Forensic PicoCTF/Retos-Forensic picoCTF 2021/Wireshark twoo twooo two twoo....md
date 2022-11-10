	# Wireshark twoo twooo two twoo...
## Objetivo
Can you find the flag? [shark2.pcapng](https://mercury.picoctf.net/static/7b8e53329b34946177a9b5f2860a0292/shark2.pcapng).

## Soluciòn
primero vemos de que tipo es el archivo shark2 
```shell

┌──(kali㉿kali)-[~/Downloads]
└─$ file shark2.pcapng
shark2.pcapng: pcapng capture file - version 1.0
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ wireshark  shark2.pcapng 
 ** (wireshark:198212) 20:42:53.824819 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 6312, resource id: 22482789, major code: 40 (TranslateCoords), minor code: 0

'despues nos abrira el programa en el nos vamos a la pestaña file y exportamos en csv'


┌──(kali㉿kali)-[~/Downloads]
└─$ cat flag-shark2.csv | cut -d ' ' -f 5 | cut -d '.' -f1 | tr -d '\n' | base64 -d
picoCTF{dns_3xf1l_ftw_deadbeef}                                                                                                                                                                       

```
picoCTF{dns_3xf1l_ftw_deadbeef}

## Referencias
- []()