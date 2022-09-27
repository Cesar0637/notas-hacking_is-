# Wave a flag

## Objetivo 

## Descripcion
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...

---
## Solución 
Primero le damos permisos de administrador 
chmod 777 warm 
Despues lo abrimos 
┌──(kali㉿kali)-[~/Downloads]
└─$ ./warm -h               
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}


## Notas
si no se puede abrir un archivo hay que revisar que permisos se tienen
## Referencias
