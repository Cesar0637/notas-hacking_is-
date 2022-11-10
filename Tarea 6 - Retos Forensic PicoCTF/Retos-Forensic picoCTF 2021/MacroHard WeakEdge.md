# MacroHard WeakEdge
## Objetivo
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/2e739f9e0dc9f4c1556ea6b033c3ec8e/Forensics is fun.pptm)

## Soluciòn
primero descomprimimos el archivo 
nos derigimos hasta slide masters 
abrimos el archivo hidden 
y despues lo convertimos para que nos de la bandera

```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ cd ppt 
                                                                             
┌──(kali㉿kali)-[~/Downloads/ppt]
└─$ cd slideMasters
                                                                             
┌──(kali㉿kali)-[~/Downloads/ppt/slideMasters]
└─$ cat hidden     
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                             
┌──(kali㉿kali)-[~/Downloads/ppt/slideMasters]
└─$ cat hidden | tr -d ' ' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
                                     
```
picoCTF{D1d_u_kn0w_ppts_r_z1p5}

## Referencias
- []()