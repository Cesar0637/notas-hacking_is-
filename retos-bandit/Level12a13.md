#Bandit
##Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
##Datos de acceso
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

##solucion
bandit12@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 May  7  2020 .
drwxr-xr-x 41 root     root     4096 May  7  2020 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
-rw-r-----  1 bandit13 bandit12 2582 May  7  2020 data.txt
-rw-r--r--  1 root     root      675 May 15  2017 .profile
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
##Notas adicionales
usar zcat, bzcat y tar xO para traducir 
##Referencias 

