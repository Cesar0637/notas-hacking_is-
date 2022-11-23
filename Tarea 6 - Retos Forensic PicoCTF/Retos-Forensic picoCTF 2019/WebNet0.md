# WebNet0
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Soluciòn
cargamos la llave en wireshark
en la barra de herramientas/edit/Preferences/Protocols
Buscamos el que es **TLS**
En la parte que dice RSA keys list damos click en Edit
nos arrojara una tabla vamos a key file lo clickeamos y buscamos la llave 
Ahora nos muestra los paquetes HTTP, si lo seguimos (click secundario>Follow>HTTP Stream)

picoCTF{nongshim.shrimp.crackers}



## Referencias
- []()