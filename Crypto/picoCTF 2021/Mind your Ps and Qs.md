# Mind your Ps and Qs
## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values)

## Soluciòn
este es bastante similar a los rsa utilzaremos las mismas formulas empleadas 
```python
>>>c=81324412343527190895777142537838333832920579264010533029282104230006461420086153423
>>> e=65537
>>> p=1246543322237890492055221842734816092141
>>> q=65444433217509699665091201633524389157003
>>> n = p * q
>>> n
1122344432562595991877980619849724606784164430105441327897358800116889057763413423
>>> tn = (p-1)*(q-1)
>>> from Crypto.Util.number import inverse
>>> d=inverse(e,tn)
>>> from Crypto.Util.number import long_to_bytes
>>> m=pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_13681467}'
>>>
```

## Referencias
- []()