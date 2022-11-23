# m00nwalk
## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.

## Soluciòn

tenemos que ir ala dirrecion opt para instalar una herramienta 
```shell
┌──(kali㉿kali)-[~]
└─$ cd /opt
                                                                             
┌──(kali㉿kali)-[/opt]
└─$ sudo git clone https://github.com/colaclanth/sstv.git
[sudo] password for kali: 
Cloning into 'sstv'...
remote: Enumerating objects: 221, done.
remote: Total 221 (delta 0), reused 0 (delta 0), pack-reused 221
Receiving objects: 100% (221/221), 1.01 MiB | 2.36 MiB/s, done.
Resolving deltas: 100% (140/140), done.
                                                                             
┌──(kali㉿kali)-[/opt]
└─$ cd sstv        
                                                                             
┌──(kali㉿kali)-[/opt/sstv]
└─$ sudo python setup.py install
running install ...
...
Finished processing dependencies for sstv==0.1
                                                                             
┌──(kali㉿kali)-[/opt/sstv]
└─$ cd ..   
                                                                             
┌──(kali㉿kali)-[/opt]
└─$ cd ..

                                 
  
┌──(kali㉿kali)-[/]
└─$ cd home     
                                                                             
┌──(kali㉿kali)-[/home]
└─$ cd kali/Downloads 
                                                     ```
Ahora ejecutamos los siguientes comandos que obtuvimos gracias ala herramienta que instalamos en la imagen que descargamos para decodificarla  por ultimo abrimos la imagen resultante
```shell                        
┌──(kali㉿kali)-[~/Downloads]
└─$ sstv -d message.wav -o message-resultado.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [###########################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ open message-resultado.png

```
picoCTF{beep_boop_im_in_space}

## Referencias
- []()