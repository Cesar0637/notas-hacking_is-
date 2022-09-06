Bandit
##Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
##Datos de acceso 
bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
##solucion
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z][n-za-nN-ZA-N]
tr: missing operand after ‘[a-zA-Z][n-za-nN-ZA-N]’
Two strings must be given when translating.
Try 'tr --help' for more information.
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

##Notas adicionales
Podemos desifrar  con el  comando cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
##Referencias 

