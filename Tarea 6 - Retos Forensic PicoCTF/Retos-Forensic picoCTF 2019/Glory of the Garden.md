# Glory of the Garden
## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.

## Soluciòn

La mejor solucion y mas raida es usando un grep 

```shell
┌──(kali㉿kali)-[~]
└─$ cd Downloads 
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ strings garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"

```
picoCTF{more_than_m33ts_the_3y33dd2eEF5}

## Referencias
- []()