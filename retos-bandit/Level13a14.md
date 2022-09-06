#Bandit
##Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
##Datos de acceso 
bandit13
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
##solucion

bandit13@bandit:~$ cat sshkey.private

-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkO......


//Guardamos la clave en un archivo

$ nano llave14


$ ls -la llave14
$ chmod 600 llave14
$ ls -la llave14
-rw-r--r-- 1 HP 197121 1679 Sep  4 20:25 llave14
// Volvemos a entrar al bandit

bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

##Notas adicionales
el comando -i de ssh para poder usar un archivo de clave primaria y poder entrar con ella.
##Referencias 

