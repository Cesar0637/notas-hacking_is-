#Bandit
##Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
##Datos de acceso 
bandit11
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
##solucion
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
bandit10@bandit:~$ cat data.txt | base64 -d
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

##Notas adicionales
Con base64 -d podemops pasar a base 64
##Referencias 
https://en.wikipedia.org/wiki/Base64

