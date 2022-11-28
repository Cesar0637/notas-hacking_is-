# Pixelated
## Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/e8054e22552c6aba591cdf7440eb25e4/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/e8054e22552c6aba591cdf7440eb25e4/scrambled2.png)

## Soluciòn
creamos el siguiente escript de pyton para poder funcionar las imagenes y listo
```shell

┌──(kali㉿kali)-[~/Downloads]
└─$ python exp.py


┌──(kali㉿kali)-[~/Downloads]
└─$ open nueva.png

```

```python
from PIL import Image
import numpy as np

img1=np.asarray(Image.open('scrambled1.png'))
img2=np.asarray(Image.open('scrambled2.png'))

print(img1)
print(img2)

datos=img1.copy() + img2.copy()

nueva = Image.fromarray(datos)

nueva.save('nueva.png','PNG')
```



picoCTF{d32ea5ac}

## Referencias
- []()
