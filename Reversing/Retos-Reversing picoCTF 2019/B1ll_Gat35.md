# B1ll_Gat35
## Objetivo
Can you reverse this [Windows Binary](https://jupiter.challenges.picoctf.org/static/0ef5d0d6d552cd5e0bd60c2adbddaa94/win-exec-1.exe)?

## Soluciòn
corri el archivo desde windows 
pide contraseña para dar la bandera asi esque con ghidra
vamos a modificarlo, en la seccion del if cambiamos el salto JZ por JC que basicamente es sin condicion para poder pasar directo ala respues
exportamos el programa y lo volvi abrir con windows
```shell

C:\Users\Cesar\Documents\GitHub\notas-hacking_is->list
"list" no se reconoce como un comando interno o externo,
programa o archivo por lotes ejecutable.

C:\Users\Cesar\Documents\GitHub\notas-hacking_is->C:\Users\Cesar\Documents\GitHub\notas-hacking_is-\win-exec-2.exe
Input a number between 1 and 5 digits: 1
Initializing...
Enter the correct key to get the access codes: 23
Correct input. Printing flag: PICOCTF{These are the access codes to the vault: 1063340}
C:\Users\Cesar\Documents\GitHub\notas-hacking_is->


```
PICOCTF{These are the access codes to the vault: 1063340}

## Referencias
- []()
