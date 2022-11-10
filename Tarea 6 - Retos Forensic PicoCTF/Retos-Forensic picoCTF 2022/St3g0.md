# St3g0
## Objetivo
Download this image and find the flag.

-   [Download image](https://artifacts.picoctf.net/c/423/pico.flag.png)

## Soluciòn
```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ zsteg -a -v pico.flag.png
zsteg: command not found
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ sudo gem install zsteg       
[sudo] password for kali: 
Fetching rainbow-3.1.1.gem
Fetching zsteg-0.2.11.gem
Fetching zpng-0.4.3.gem
Fetching iostruct-0.0.4.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.3
Successfully installed iostruct-0.0.4
Successfully installed zsteg-0.2.11
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.3
Installing ri documentation for zpng-0.4.3
^[[B^[[B^[[B^[[B^[[B^[[B^[[B^[[B^[[BParsing documentation for iostruct-0.0.4
Installing ri documentation for iostruct-0.0.4
Parsing documentation for zsteg-0.2.11
Installing ri documentation for zsteg-0.2.11
Done installing documentation for rainbow, zpng, iostruct, zsteg after 1 seconds
4 gems installed
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ steg -a -v pico.flag.png
Command 'steg' not found, did you mean:
  command 'stg' from deb stgit
  command 'step' from deb step
Try: sudo apt install <deb name>
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ zsteg -a -v pico.flag.png
b1,r,lsb,xy         .. text: "~__B>wV_G@"
    00000000: 5e 35 3f 06 7e 5f 5f 42  3e 77 56 5f 47 40 00 00  |^5?.~__B>wV_G@..|
    00000010: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    00000050: 00 04 ff ff ff f9 00 00  00 00 00 00 00 00 00 00  |................|
    00000060: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    00000090: 00 00 00 00 00 00 00 00  00 00 1f ff ff ff ff f8  |................|
    000000a0: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    000000e0: 00 00 00 7f ff ff ff ff  fe c0                    |..........      |
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_96ae0ac1}$t3g0"
    00000000: 70 69 63 6f 43 54 46 7b  37 68 33 72 33 5f 31 35  |picoCTF{7h3r3_15|
    00000010: 5f 6e 30 5f 35 70 30 30  6e 5f 39 36 61 65 30 61  |_n0_5p00n_96ae0a|
    00000020: 63 31 7d 24 74 33 67 30  00 00 00 00 00 00 00 00  |c1}$t3g0........|
    00000030: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    000000f0: 00 00 00 00 01 42 f3 6d  b6 db 6d b6 db 6d b6 db  |.....B.m..m..m..|

```
picoCTF{7h3r3_15_n0_5p00n_96ae0ac1}

## Referencias
- []()