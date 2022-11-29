# Need For Speed
## Objetivo
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed).

## Soluciòn
```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ chmod a+x need-for-speed
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ ./need-for-speed        
Keep this thing over 50 mph!
============================

Creating key...
Not fast enough. BOOM!
                          
┌──(kali㉿kali)-[~/Downloads]
└─$ objdump -D need-for-speed -M intel | grep '<main>:' -A20
000000000000091a <main>:
 91a:   55                      push   rbp
 91b:   48 89 e5                mov    rbp,rsp
 91e:   48 83 ec 10             sub    rsp,0x10
 922:   89 7d fc                mov    DWORD PTR [rbp-0x4],edi
 ...
0000000000000960 <__libc_csu_init>:

┌──(kali㉿kali)-[~/Downloads]
└─$ sudo apt install gdb
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
....
┌──(kali㉿kali)-[~/Downloads]
└─$ gdb ./need-for-speed
GNU gdb (Debian 12.1-4) 12.1
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from ./need-for-speed...
(No debugging symbols found in ./need-for-speed)
(gdb) break set_timer
Breakpoint 1 at 0x833
(gdb) r
Starting program: /home/kali/Downloads/need-for-speed 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
Keep this thing over 50 mph!
============================


Breakpoint 1, 0x0000555555400833 in set_timer ()
(gdb) return
Make selected stack frame return now? (y or n) y
#0  0x000055555540093d in main ()
(gdb) step
Single stepping until exit from function main,
which has no line number information.
Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #190ca38b speeding along!}
__libc_start_call_main (main=main@entry=0x55555540091a <main>, argc=argc@entry=1, argv=argv@entry=0x7fffffffe028) at ../sysdeps/nptl/libc_start_call_main.h:74
74      ../sysdeps/nptl/libc_start_call_main.h: No such file or directory.
(gdb) 

```
PICOCTF{Good job keeping bus #190ca38b speeding along!}

## Referencias
- []()
