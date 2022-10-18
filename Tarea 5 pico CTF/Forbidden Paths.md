
## Objetivo
Can you get the flag? Here's the [website](http://saturn.picoctf.net:55827/). We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?

## Soluciòn

tenemos que buscar el archivo que tiene la bandera 
intentamos con flag.txt y no la encuentra 
si intentamos con la siguiente estructura: **../../../../flag.txt** 


picoCTF{7h3_p47h_70_5ucc355_6db46514}

## Referencias
- []()