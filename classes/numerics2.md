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

### Com s'implementa la resta?

El "*complement a un*" i el "*complement a dos*" són dues eines matemàtiques que faciliten molt les tasques aritmètiques en el sistema binari, sobretot la realització de restes i el treball amb nombres negatius.

El "complement a un" (C1) d’un nombre binari és el nombre resultant d’invertir els uns i els zeros d’aquest nombre. Per exemple, el complement a un del nombre `1101` és el nombre `0010`.

El "complement a dos" (C2) d’un nombre binari és el nombre resultant de sumar 1 al seu complement a un. És a dir, C2 = C1 + 1. Generalment s’assumeix que el C2 és la manera de representar el negatiu d’un número binari.

Llavors, la **resta de dos nombres binaris pot obtenir-se sumant al minuend el complement a dos del subtrahend**.

+ Escriu un algorisme que resti dos nombres binaris que estan emmagatzemats en dues llistes: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb )
+ Quina és la complexitat de l'algorisme?

---

### Video: Fibonacci.

Video de 7' sobre l'arribada a Europa del sistema decimal i el paper que hi va jugar Fibonacci. Definició i algorisme per calcular la célebre serie de Fibonaci. 

<center>
<iframe src="https://drive.google.com/file/d/1cG7MLI_8ZfmBhskfOFjDGQiz2A-khsdI/preview" width="640" height="480"></iframe>
</center>

---

### Exercicis: Algorisme de Fibonacci

```python
def fib1(n):
    if n==0:
        return n
    if n==1:
        return n
    else:
        return fib1(n-1) + fib1(n-2)
```        

+ Copia l'algorisme recursiu de Fibonacci a un notebook i calcula el terme 10 i el terme 100: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb ) 
+ Què ha passat quan has intentat calcular el terme 100? Per què?

---

### Video: Recursivitat.

Video de 8' sobre el càlcul **recursiu** de l'algorisme de Fibonacci.

<center>
<iframe src="https://drive.google.com/file/d/16-93vRppB7LHWZnHGA3VKQwrXAtnxV1u/preview" width="640" height="480"></iframe>
</center>

---


### Video: Altres versions de Fibonacci.

Video de 7' sobre el càlcul **no recursiu** de l'algorisme de Fibonacci.

<center>
<iframe src="https://drive.google.com/file/d/1KJMnTY5SkJd-Afhdl2aKaPBCmUbR91e4/preview" width="640" height="480"></iframe>
</center>


---


### Exercici: Un algorisme eficient per calcular els termes de la sèrie de Fibonacci

```python
def fib3(n):
    a,b = 0,1
    for i in range(1,n+1):
        a,b = b, a+b
    return a

fib3(10)
> 55
```

+ Executeu aquest algorisme amb l'eina [Code Skulptor](http://www.codeskulptor.org/viz/index.html). Aquesta eina us permet visualitzar fàcilment el funcionament de qualsevol algorisme. Familiaritzeu-vos amb ella, perquè us pot ser útil.



---

### Video: **Passos computacionals** d'un algorisme


Video de 3' amb la introducció al càlcul del cost computacional d'un algorisme.

<center>
<iframe src="https://drive.google.com/file/d/1lg4m74ZPplqSxRi3ufmPldUxo8Z61NJk/preview" width="640" height="480"></iframe>
</center>


---

### Exercicis

+ Escriu un algorisme que divideixi (ens retorni el quocient de) dos nombres enters, positius i més grans que 1, sense fer servir els operadors de multiplicació `*`, divisió `/` ni mòdul `%`: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb )

+ Contesta les següents preguntes:
  + Quantes operacions (assignacions, comparacions, sumes i restes) fa quan calcula `90/10`?


---
### Video: La notació Gran O


Video de 7' amb una introducció a la notació Gran O

<center>
<iframe src="https://drive.google.com/file/d/1xGyM79UACMCNFKugtd1Em-0g2LCMggUp/preview" width="640" height="480"></iframe>
</center>


---



### Material addicional. 



És important familiaritzar-se amb les magnituds dels nombres per entendre quan és viable que un ordinador calculi alguna cosa. 

Aquest video, us pot ajudar a tenir una idea intuitiva de la magnitud de les potències de 10. 

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/0fKBhvDjuy0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

