# WebNet1
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Soluciòn
este es similar al anterior 
```shell
┌──(kali㉿kali)-[~/Downloads]

└─$ ssldump -r capture4.pcap -k picopico2.key -d > output 

┌──(kali㉿kali)-[~/Downloads]
└─$ ssldump -r capture4.pcap -k picopico2.key -d         
New TCP connection #1: 128.237.140.23(57930) <-> 172.31.22.220(443)
1 1  0.0297 (0.0297)  C>S  Handshake
      ClientHello
        Version 3.3 
        cipher suites
        TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
        TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384

```
picoCTF{this.is.not.your.flag.anymore}--- saldrà esta, pero no es la flag.

picoCTF{honey.roasted.peanuts}--- esta sì es la flag.

## Referencias
- []()