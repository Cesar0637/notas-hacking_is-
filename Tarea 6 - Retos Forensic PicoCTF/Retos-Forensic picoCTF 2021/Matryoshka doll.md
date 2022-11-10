# Matryoshka doll
## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/b6205dd933ec01c022c4e6acbdf11116/dolls.jpg)

## Soluciòn
la imagen contenia una muñeca rusa asi esque iremos capa por capa con el comando binwalk hasta llegar al flag.txt, hacemos un cat para poder ver la bandera.

```shell
┌──(kali㉿kali)-[~]
└─$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls Downloads 
dolls.jpg                Retos-Kali--picoCTF-AICE-main.zip
Obsidian-1.0.3.AppImage  Tarea6
                                                                             
┌──(kali㉿kali)-[~]
└─$ file dolls.jpg          
dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced

┌──(kali㉿kali)-[~]
└─$ ls          
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls Downloads
dolls.jpg               main.zip
Obsidian-1.0.3.AppImage  Tarea6
                                                                             
┌──(kali㉿kali)-[~]
└─$ open dolls.jpg
                                                                             
┌──(kali㉿kali)-[~]
└─$ cd Downloads 
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ file dolls.jpg
dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ open dolls.jpg
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ binwalk dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378952, uncompressed size: 383937, name: base_images/2_c.jpg
651610        0x9F15A         End of Zip archive, footer length: 22

                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378952, uncompressed size: 383937, name: base_images/2_c.jpg
651610        0x9F15A         End of Zip archive, footer length: 22

                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ cd _dolls.jpg.extracted/ls
cd: no such file or directory: _dolls.jpg.extracted/ls
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ cd _dolls.jpg.extracted/  
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted]
└─$ ls          
4286C.zip  base_images
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted]
└─$ cd base_images          
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images]
└─$ open 2_c.jpg  
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images]
└─$ binwalk -e 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images]
└─$ ls _2_c.jpg.extracted 
2DD3B.zip  base_images
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images]
└─$ ls                   
2_c.jpg  _2_c.jpg.extracted
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images]
└─$ cd _2_c.jpg.extracted/            
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ ls
2DD3B.zip  base_images
                                                                             
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ cd base_images        
                                                                             
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg
                                                                             
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ binwalk -e 3_c.jpg  

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79807, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

                                                                             
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ cd _3_c.jpg.extracted/ 
                                                                             
┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ cd base_images 
                                                                             
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 63, uncompressed size: 81, name: flag.txt
79785         0x137A9         End of Zip archive, footer length: 22

                                                                             
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 
                                                                             
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls
136DA.zip  flag.txt
                                                                             
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ open flag.txt 
                                                                             
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt 
picoCTF{96fac089316e094d41ea046900197662}                                                                             
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ 
```
picoCTF{96fac089316e094d41ea046900197662}  

## Referencias
- []()