
## Objetivo
Connect to this PostgreSQL server and find the flag!
**This challenge launches an instance on demand.**

## Soluciòn
primero le damos click a lanzar instancia 
 en la descripciòn de este reto nos darà un comando para poder acceder a la base de datos
```shell
┌──(kali㉿kali)-[~/Desktop/CarpetaCompartida.Windows]
└─$ psql -h saturn.picoctf.net -p 65078 -U postgres pico
Password for user postgres: 
psql (14.4 (Debian 14.4-1+b1), server 14.2 (Debian 14.2-1.pgdg110+1))
Type "help" for help.
```
despues con el comando /d vemos las tablas que hay
``` shell
pico=# \d
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
```
por ultimo con el comando select mandamos a traer todos los elementos en la tabla 
```shell
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# exit


```
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}

## Referencias
- []()