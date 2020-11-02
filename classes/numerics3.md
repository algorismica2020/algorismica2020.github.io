# Sessió en línia del dia 2/11/2020: Algorismes Numèrics III

Aquesta sessió té una durada aproximada de 60 minuts i està formada per alguns videos sobre els aspectes teòrics del tema i diversos exercicis. 
Es recomana seguir aquests continguts en el mateix ordre que apareixen en aquesta pàgina.

Els apunts complets d'aquest tema es poden veure [aquí](https://algorismica2020.github.io/slides/numerics2.html)  

> **AVÍS**: Recordeu que si voleu conservar els notebooks que obriu des d'aquesta pàgina heu de baixar-los al vostre ordinador abans de tancar Colab.


---
### L'algorisme d'Euclides

La forma més obvia de trobar el **màxim comú divisor** de dos nombres és trobar els factors dels dos nombres i multiplicar llavors els seus factors comuns. Per exemple, el mcd de `1035` i `759`:

> `1035 = 3^2*5*23`  i  `759 = 3*11*23`, per tant `mcd = 3*23 = 69`
 
El problema és que **no es coneix** cap algorisme eficient per **factoritzar** els nombres: No hi ha cap algorisme publicat per poder factoritzar-lo en temps polinòmic, és a dir, no existeix cap algorisme publicat que pugui factoritzar-lo en temps `O(n^k)` independentment de quina sigui la constant `k`.

Fa més de 2000 anys que Euclides va enunciar un algorisme alternatiu per trobar el màxim comú divisor de dos nombres `a` i `b`.

```python
def mcd(a,b):
    while a:      # aquí es fa un truc, si 'a!=0', 'a' s'avalua com a True
        a,b = b%a, a
    return b

mcd(1071, 462)
> 21
```

#### Quina complexitat té per nombres grans?

La primera cosa que hem de veure és quantes vegades s'executa el `while`, o el que és el mateix, com es van reduint els nombres a mesura que anem calculant.

> Cal fixar-se que a cada iteració els arguments `(a,b)` es converteixen a `(b mod a, a)`: canviem l’ordre i el més gran queda reduït al mòdul del petit.

> Es pot demostrar que això vol dir que **en dues iteracions successives els dos arguments decreixen al menys a la meitat**, és a dir, perden un bit en la seva representació.


Per tant, si inicialment eren enters de `n` bits, en `2n` iteracions arribarem al final de l’algorisme. Com que cada iteració implica una divisió d’ordre quadràtic, `(a mod b)` , el temps total serà `O(n^3)`.

---

### Test de primeritat

Video de 20' sobre el test de primeritat. 

<center>
<iframe src="https://drive.google.com/file/d/10jEVSRbG61xc3mU-RFj2qV-sUcLew5fy/preview" width="640" height="480"></iframe>
</center>

---

### Cerca de nombres primers grans

Video de 5' sobre la complexitat de trobar nombres primers grans. 

<center>
<iframe src="https://drive.google.com/file/d/1AARAQIqGfl6vNplDV2-UyMMctSVtA-kU/preview" width="640" height="480"></iframe>
</center>

---

### Recapitulació sobre aritmètica modular i criptografia

Video de 5' sobre la complexitat de l'aritmètica modular i la criptografia. 

<center>
<iframe src="https://drive.google.com/file/d/1e6y6_vnWojrN_clYpFMh-i-rFmixt3MJ/preview" width="640" height="480"> </iframe>
</center>
