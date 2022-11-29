# vault-door-1
## Objetivo
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/ff2585f7afd21b81f69d2fbe37c081ae/VaultDoor1.java)

## Soluciòn
al abrir el archivo nos damos cuenta que para verificar el password verifica cada caracter uno por uno,  hay mismo podemos armar la bandera pero no esta en orden y seria muy tardado armarla asi.
Hay que guardar cada verificacion en un archivo que en est caso llamaremos vaultTempo y aplicamos estos comandos

```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ cat vaultTemp|sort|awk '{print($3)}'|tr -d "'"|tr -d '\n'|tr -d ';' 
d35cr4mbl3d_tH3_cH4r4cT3r5_f6daf4                                                                                
```
picoCTF{d35cr4mbl3d_tH3_cH4r4cT3r5_f6daf4}   
## Referencias
- []()