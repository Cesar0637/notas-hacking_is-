
## Objetivo
We have several pages hidden. Can you find the one with the flag? The website is running [here](http://saturn.picoctf.net:49917/).

## Soluciòn
usando el comando Wfuzz en la pagina nos damos cuenta 
hay un elemento llamado secret lo usamos unas veces hatsa que llegamos a  "http://saturn.picoctf.net:61481/secret/hidden/superhidden/   hay en ese punto podemos ver la bandera

```shell


┌──(kali㉿kali)-
└─$ curl "http://saturn.picoctf.net:61481/secret/hidden/superhidden/index.html"
<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <link rel="stylesheet" href="mycss.css" />
  </head>

  <body>
    <h1>Finally. You found me. But can you see me</h1>
    <h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_790d2615}</h3>
  </body>
</html>

┌──(kali㉿kali)-
└─$ 
```
picoCTF{succ3ss_@h3n1c@10n_790d2615}

## Referencias
- []()