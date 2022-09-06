# Bandit
## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1

## Solucion

bandit16@bandit:~$ nmap -p31000-32000 localhost

bandit16@bandit:~$ openssl s_client -connect localhost:31790

JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOk.......

nano llave17
$ ls -la llave17
-rw-r--r-- 1 HP 197121 1675 Sep  5 01:28 llave17
$ chmod 600 llave17
$ ls -la llave17
$ ssh -i llave17 bandit17@bandit.labs.overthewire.org -p 2220
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## Notas adicionales
nmap es un escaneo de puertos

