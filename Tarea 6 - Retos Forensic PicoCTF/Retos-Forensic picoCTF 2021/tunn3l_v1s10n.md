# tunn3l_v1s10n
## Objetivo
We found this [file](https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l_v1s10n). Recover the flag.

## Soluciòn


```shell

┌──(kali㉿kali)-[~/…]
└─$ file tunn3l_v1s10n 
tunn3l_v1s10n: data

┌──(kali㉿kali)-[~/…
└─$ xxd -g1 tunn3l_v1s10n | head
00000000: 42 4d 8e 26 2c 00 00 00 00 00 ba d0 00 00 ba d0  BM.&,...........

┌──(kali㉿kali)-[~/
└─$ xxd -g1 tunn3l_v1s10n | head
00000000: 42 4d 8e 26 2c 00 00 00 00 00 28 00 00 00 28 00  BM.&,.....(...(.

┌──(kali㉿kali)-[~
└─$ file tunn3l_v1s10n          
tunn3l_v1s10n: PC bitmap, Windows 3.x format, 1134 x 306 x 24, image size 2893400, resolution 5669 x 5669 px/m, cbSize 2893454, bits offset 40

┌──(kali㉿kali)-[~/
└─$ xxd -g1 tunn3l_v1s10n | head
00000000: 42 4d 8e 26 2c 00 00 00 00 00 28 00 00 00 28 00  BM.&,.....(...(.
00000010: 00 00 6e 04 00 00 32 01 00 00 01 00 18 00 00 00  ..n...2.........

┌──(kali㉿kali)-[~
└─$ xxd -g1 tunn3l_v1s10n | head
00000000: 42 4d 8e 26 2c 00 00 00 00 00 28 00 00 00 28 00  BM.&,.....(...(.
00000010: 00 00 6e 04 00 00 40 03 00 00 01 00 18 00 00 00  ..n...@.........

```

hay que aumentar el tamaño de la imagen y veremos la bandera
picoCTF{qu1t3_a_v13w_2020}

## Referencias
- []()