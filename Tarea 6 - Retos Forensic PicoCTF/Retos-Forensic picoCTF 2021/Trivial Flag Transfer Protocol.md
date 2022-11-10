# Trivial Flag Transfer Protocol
## Objetivo
Figure out how they moved the [flag](https://mercury.picoctf.net/static/fb24ddcfaf1e297be525ba7474964fa5/tftp.pcapng).

## Soluciòn


```shell
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ file tftp.pcapng
tftp.pcapng: pcapng capture file - version 1.0
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ wireshark tftp.pcapng  
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ cat instructions.txt | tr [A-Z] [N-ZA-M]
cat: instructions.txt: No such file or directory
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ wireshark tftp.pcapng                   
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ cat instructions.txt | tr [A-Z] [N-ZA-M]
TFTPDOESNTENCRYPTOURTRAFFICSOWEMUSTDISGUISEOURFLAGTRANSFER.FIGUREOUTAWAYTOHIDETHEFLAGANDIWILLCHECKBACKFORTHEPLAN
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$  cat plan | tr [A-Z] [N-ZA-M]
IUSEDTHEPROGRAMANDHIDITWITH-DUEDILIGENCE.CHECKOUTTHEPHOTOS
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ file program.deb  
program.deb: Debian binary package (format 2.0), with control.tar.gz, data compression xz
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ file program.deb
program.deb: Debian binary package (format 2.0), with control.tar.gz, data compression xz
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ dpkg-deb -I program.deb
 new Debian package, version 2.0.
 size 138310 bytes: control archive=1250 bytes.
     826 bytes,    18 lines      control              
    1184 bytes,    17 lines      md5sums              
 Package: steghide
 Source: steghide (0.5.1-9.1)
 Version: 0.5.1-9.1+b1
 Architecture: amd64
 Maintainer: Ola Lundqvist <opal@debian.org>
 Installed-Size: 426
 Depends: libc6 (>= 2.2.5), libgcc1 (>= 1:4.1.1), libjpeg62-turbo (>= 1:1.3.1), libmcrypt4, libmhash2, libstdc++6 (>= 4.9), zlib1g (>= 1:1.1.4)
 Section: misc
 Priority: optional
 Description: A steganography hiding tool
  Steghide is steganography program which hides bits of a data file
  in some of the least significant bits of another file in such a way
  that the existence of the data file is not visible and cannot be proven.
  .
  Steghide is designed to be portable and configurable and features hiding
  data in bmp, wav and au files, blowfish encryption, MD5 hashing of
  passphrases to blowfish keys, and pseudo-random distribution of hidden bits
  in the container data.
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ open picture1.bmp 

┌──(kali㉿kali)-[~/Downloads]
└─$ ls
'01- Matryoshka doll.md'     '04- Trivial Flag Transfer Protocol.md'   docProps              'Forensics is fun.pptm'   plan          _rels
'02- tunn3l_v1s10n.md'       '0n- Nombre 1 3.md'                       dolls.jpg              instructions.txt         ppt           tftp.pcapng
'03- MacroHard WeakEdge.md'  '[Content_Types].xml'                     _dolls.jpg.extracted   picture1.bmp             program.deb   tunn3l_v1s10n

┌──(kali㉿kali)-[~/Downloads]
└─$ cat instructions.txt
GSGCQBRFAGRAPELCGBHEGENSSVPFBJRZHFGQVFTHVFRBHESYNTGENAFSRE.SVTHERBHGNJNLGBUVQRGURSYNTNAQVJVYYPURPXONPXSBEGURCYNA



┌──(kali㉿kali)-[~/Downloads]
└─$ steghide --extract -sf picture3.bmp -p DUEDILIGENCE
wrote extracted data to "flag.txt".

┌──(kali㉿kali)-[~/Downloads]
└─$ cat flag.txt                

```
picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
## Referencias
- []()