## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)

## Soluciòn
lemeos el archivo values
viendo la n vemos que es pequeña
la refactorizamos 
despues aplicamos la formula y listo


>>> c=843044897663847841476319711639772861390329326681532977209935413827620909782846667
>>> 
>>> p= 2159947535959146091116171018558446546179
>>> 
>>> q= 658558036833541874645521278345168572231473
>>> 
>>> e=65537
>>> 
>>> n= p*q 
>>> 
>>> tn = (p-1)*(q-1)
>>> 

>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> d = inverse(e,tn)
>>> d 
975120122884150896343356420256053234758228648361853546720066993334766006694511009

>>> m = pow (c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639555294957886055592061
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_00264570}'


## Referencias
- []()