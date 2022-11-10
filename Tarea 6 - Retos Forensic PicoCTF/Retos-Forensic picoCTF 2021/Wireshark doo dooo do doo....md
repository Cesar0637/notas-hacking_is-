# Wireshark doo dooo do doo...
## Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/81c7862241faf4a48bd64a858392c92b/shark1.pcapng).

## Soluciòn
vamos donde tenemos el archivo despues lo abrimos con la herramienta wireshark despues ponemos el comando tcp.stream.eq5
```shell
┌──(kali㉿kali)-[~/Downloads]
└─$ echo 'cvpbPGS{c33xno00_1_f33_h_qrnqorrs}' | tr 'A-Za-z' 'N-ZA-Mn-za-m'
picoCTF{p33kab00_1_s33_u_deadbeef}

```
picoCTF{p33kab00_1_s33_u_deadbeef}

## Referencias
- []()