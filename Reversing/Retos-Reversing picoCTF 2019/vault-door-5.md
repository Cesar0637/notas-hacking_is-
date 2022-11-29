# vault-door-5
## Objetivo
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/d31ce4356bdfd15d33a9af7e35ab4d0a/VaultDoor5.java)

## Soluciòn
en esta parte del codigo que descargamos en el reto vemos que esta en base 64
con el cyberchef lo decodificamos 
```shell

		String expected = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm"
                        + "JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2"
                        + "JTM0JTVmJTM4JTM0JTY2JTY0JTM1JTMwJTM5JTM1";

        return base64Encoded.equals(expected);
    }
}

```

JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm  JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2JTM0JTVmJTM4JTM0JTY2JTY0JTM1JTMwJTM5JTM1
decodifcamos y nos quedara asi
%63%30%6e%76%33%72%74%31%6e%67%5f%66%72%30%6d%5f%62%61%35%65%5f%36%34%5f%38%34%66%64%35%30%39%35
(en este caso use cyberchef)
ahora le aplicamos en la misma app el decodificador url
y listo ya estara la bandera solo hay que darle formato

picoCTF{c0nv3rt1ng_fr0m_ba5e_64_84fd5095}

## Referencias
- []()