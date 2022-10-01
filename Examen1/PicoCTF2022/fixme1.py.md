# fixme1.py 
## Objetivo  
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/39/fixme1.py)
## Solución  
descargamops el archivo 
lo ejecute y me dio error de identacion lo corregi con el cvopmando nano y listo 
```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ python fixme1.py 
  File "/home/kali/Downloads/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ nano fixme1.py 
                                                                                                
┌──(kali㉿kali)-[~/Downloads]
└─$ python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}

```
picoCTF{1nd3nt1ty_cr1515_6a476c8f}

## Referencias
- []()