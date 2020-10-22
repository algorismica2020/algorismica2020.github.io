# Sessió en línia del dia 26/10/2020: Algorismes Numèrics II

Aquesta sessió té una durada aproximada de 60 minuts i està formada per alguns videos sobre els aspectes teòrics del tema i diversos exercicis. 
Es recomana seguir aquests continguts en el mateix ordre que apareixen en aquesta pàgina.

Els apunts complets d'aquest tema es poden veure [aquí](https://algorismica2020.github.io/slides/numerics1.html) i [aquí](https://algorismica2020.github.io/slides/numerics2.html)  

> **AVÍS**: Recordeu que si voleu conservar els notebooks que obriu des d'aquesta pàgina heu de baixar-los al vostre ordinador abans de tancar Colab.


---
### Observació preliminar.

Suposem que tenim un conjunt amb `N` elements. Per exemple, com aquest: (`a`,`b`,`c`,`d`,`e`,`f`,`g`,`h`)

+ En base 10, això es representa amb el nombre `8`. Per tant, només cal un dígit per representar la cardinalitat d'aquest conjunt. 
+ Fixeu-vos que si tenim `k` dígits en base `b` podem representar els nombres fins a `b^k-1`.
  + Exemple: Si tinc 2 dígits en base 2, el conjunt més gran que puc representar (amb el nombre `11`) és 3.

Per tant, necessitem `\log_b(N+1)` dígits per escriure `N` en base `b`.

Demostració de la fòrmula anterior:

1.  Sabem que: `b^k-1 = N` 
2. Si passem el `-1` a l'altre costat i apliquem logaritmes a cada costat de la igualtat: `\log_b b^k = \log_b (N + 1)` ens queda: `k  = \log_b (N+1)`

Veiem un exemple: 

> `k=5, b=2` 

>	Si tenim 5 dígits en base 2, podem representar fins a `2^5 -1 = 32 - 1 = 31`.  Efectivament `1111 = 16 + 8 + 4 + 2 + 1 = 31`

>	Per altra banda, necessitarem `log_2 (31+1)` dígits per escriure `31` en base `b`, que són `5` dígits.



---


### Video: Aritmètica Bàsica.

Video de 9' sobre l'algorisme de la suma.

<center>
<iframe src="https://drive.google.com/file/d/1cWEOLgZx3O7-Ip9mc38EYoBiqNZGZg1z/preview" width="640" height="480"></iframe>
</center>

---

### Com s'implementa la resta en un ordinador?

El "*complement a un*" i el "*complement a dos*" són dues eines matemàtiques que faciliten molt les tasques aritmètiques en el sistema binari, sobretot la realització de restes i el treball amb nombres negatius.

El "complement a un" (C1) d’un nombre binari és el nombre resultant d’invertir els uns i els zeros d’aquest nombre. Per exemple, el complement a un del nombre `1101` és el nombre `0010`.

El "complement a dos" (C2) d’un nombre binari és el nombre resultant de sumar 1 al seu complement a un. És a dir, C2 = C1 + 1. Generalment s’assumeix que el C2 és la manera de representar el negatiu d’un número binari.

Llavors, la **resta de dos nombres binaris pot obtenir-se sumant al minuend el complement a dos del subtrahend**.

+ Escriu un algorisme que resti dos nombres binaris que estan emmagatzemats en dues llistes, com per exemple `[1,0,0,0,1]` i `[0,0,1,1,1]`. Fes-ho aquí: : [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb )
+ Quina és la complexitat de l'algorisme?

---

### Video: Aritmètica Bàsica.

Video de 9' sobre els algorismes de la multiplicació i la divisió.

<center>
<iframe src="https://drive.google.com/file/d/1cWEOLgZx3O7-Ip9mc38EYoBiqNZGZg1z/preview" width="640" height="480"></iframe>
</center>

---

### Versió no recursiva de l'algorisme d'Al Khwarizmi.

L'algorisme d'Al Khwarizmi es pot implementar de forma no recursiva molt fàcilment. Intenta entendre aquesta implementació, fent una simulació de l'execució a mà i després executa'l: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb ) 

```python
def mul(a,b):
    result = 0
    while b != 0:
        if (b%2) :
            result += a
        b >>= 1
        a <<= 1
    return result
```


Recorda que:
+ `b%2` calcula la resta de dividir `b` per 2. Per tant, és una expressió booleana certa si el nombre és senar i falsa si és parell. 
+ `b>>=1` opera a nivell de bits i simplement desplaça la representació de `b` un bit cap a l'esquerra. Això és equivalent a dividir `b` per 2, amb cost `O(n)`. 
+ `a<<=1` opera a nivell de bits i simplement desplaça la representació de `a` un bit cap a la dreta. Això és equivalent a multiplicar `a` per 2, amb cost `O(n)`.


---



