# credstuff
## Objetivo
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://artifacts.picoctf.net/c/534/leak.tar). The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

## Soluciòn
```shell
──(kali㉿kali)-[~/Downloads]
└─$ tar -tvf leak.tar
drwxr-xr-x root/root         0 2022-03-15 02:29 leak/
-rwxr-xr-x root/root     13130 2022-03-15 02:29 leak/passwords.txt
-rwxr-xr-x root/root      7531 2022-03-15 02:29 leak/usernames.txt
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ tar -xvf leak.tar
leak/
leak/passwords.txt
leak/usernames.txt
                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ cd leak     
                    
┌──(kali㉿kali)-[~/Downloads/leak]
└─$ echo "cvpbPGS{P7e1S_54I35_71Z3}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
picoCTF{C7r1F_54V35_71M3}

```

picoCTF{C7r1F_54V35_71M3}

## Referencias
- []()