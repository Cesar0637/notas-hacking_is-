# reverse_cipher
## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this). Can you reverse the flag.

## Soluciòn
```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ cat rev_this
picoCTF{w1{1wq84fb<1>49}     

┌──(kali㉿kali)-[~/Downloads] 
└─$ cat rev     
ELF>�@X:@8
          @@@@h���xx==   ���-�=�=px�-�=�=����DDP�tdx x x ...
          
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ cat rev | wc
      5      75   16856
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ nano solve.py
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ python solve.py 
picoCTF{r3v3rs312528e05}
                                                                                
```

Solve.py
```python
import os
import mmap

def memory_map(filename, access=mmap.ACCESS_READ):
    size = os.path.getsize(filename)
    fd = os.open(filename, os.O_RDONLY)
    return mmap.mmap(fd, size, access=access)

with memory_map("rev_this") as bin_file:
    for i in range(8):
        print(chr(bin_file[i]), end = '')
    for i in range(8, 23):
        if (i & 1) == 0:
            print(chr(bin_file[i] - 5), end = '')
        else:
            print(chr(bin_file[i] + 2), end = '')
    print (chr(bin_file[23]))
                                                                                                                                                            ```
picoCTF{r3v3rs312528e05}
## Referencias
- []()