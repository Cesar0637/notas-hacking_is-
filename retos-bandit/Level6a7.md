#Bandit
##Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
##Datos de acceso
bandit6 
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
##solucion
bandit6@bandit:/$ find / -user bandit7 -group bandit6  -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:/$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
bandit6@bandit:/$
##Notas adicionales
con el user group y size puedes ver archivos del tal usuario de tal grupo y de tal tamaño
##Referencias 

