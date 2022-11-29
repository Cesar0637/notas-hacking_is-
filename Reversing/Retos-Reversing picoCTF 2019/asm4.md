# asm4
## Objetivo
What will asm4("picoCTF_f97bb") return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/76ef117df9226a8a9306a8865b14068e/test.S)

## Soluciòn
es un codigo como los anteriores 
para ejecutarlo hay que cortarle las lines con el siguiente comando 
tambien hay que editarlo con editro de texto, en los saltos hay que dejar la expresion sola

```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ cat test.S | cut -d ':' -f2

┌──(kali㉿kali)-[~/Downloads]
└─$ nano chal.s 

┌──(kali㉿kali)-[~/…/RetosKali-exam--editar/CarpetaKali-exam1/Retos-Reversing/2019]
└─$ nano solve.c               

													┌──(kali㉿kali)-[~/Downloads]
└─$ gcc -m32 -c chal.s -o chal.o
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ gcc -m32 -c solve.c -o solve.o -w 
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ gcc -m32 -o a.out solve.o chal.o     
/usr/bin/ld: warning: chal.o: missing .note.GNU-stack section implies executable stack
/usr/bin/ld: NOTE: This behaviour is deprecated and will be removed in a future version of the linker


┌──(kali㉿kali)-[~/Downloads]
└─$ ./a.out 
Flag: 0x265


## Referencias
- []()