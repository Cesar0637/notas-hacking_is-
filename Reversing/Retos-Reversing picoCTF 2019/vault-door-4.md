# vault-door-4
## Objetivo
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/c695ee23309d453a3ef369c34cc1bccb/VaultDoor4.java)

## Soluciòn
Al descargar el archivo vaultdoor4.java lo abrimos y vemos que posiblemente la bandera este en my bytes

al pasarlo a caracteres  nos quedaria asi 
jU5t_4_bUnCh_0f_bYt3s_f4
ahora solo hay que agregar los caracteres que no estaban en charcode 
'a' , '8' , 'c' , 'd' , '8' , 'f' , '7' , 'e' 
ahora solo le damos formato
picoCTF{jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e}

## Referencias
- []()