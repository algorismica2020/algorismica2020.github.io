# Sessió en línia del dia 5/10/2020: Algorismes Numèrics I

Aquesta sessió té una durada aproximada de 90 minuts i està formada per alguns videos sobre els aspectes teòrics del tema i diversos exercicis. 
Es recomana seguir aquests continguts en el mateix ordre que apareixen en aquesta pàgina.

> **AVÍS**: Recordeu que si voleu conservar els notebooks que obriu des d'aquesta pàgina heu de baixar-los al vostre ordinador abans de tancar Colab.


---

### Video: Introducció als sistemes de numeració.

Video de 6' sobre l'història dels sistemes de numeració, la seva relació amb les operacions aritmètiques i el concepte de base de representació.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>

---

### Exercicis: Bases i Nombres

Fes els següents exercici:

+ Canvi de base:
  + Pensa com seria l'algorisme que passa un nombre escrit en base 10 a base `a`, on `a` és un nombre enter positiu qualsevol. 
  + Codifica aquest algorisme en Python: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb ) 
  + Comprova que l'algorisme és correcte fent servir aquest recurs: [https://www.rapidtables.com/convert/number/base-converter.html](https://www.rapidtables.com/convert/number/base-converter.html)
  
Intenta contestar de forma justificada les seguents preguntes:
+ Quin és el nombre enter més gran que puc representar usant 64 dígits en base 2?
+ Quin és el nombre enter més gran que puc representar usant 32 dígits en base 16?

---

### Video: Fibonacci.

Video de 6' sobre l'arribada a Europa del sistema decimal i el paper que hi va jugar Fibonacci. Definició i algorisme per calcular la célebre serie de Fibonaci. 

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>
 

---

### Video: Recursivitat.

Video de 6' sobre el càlcul **recursiu** de l'algorisme de Fibonacci.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
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


### Video: Altres versions de Fibonacci.

Video de 6' sobre el càlcul **no recursiu** de l'algorisme de Fibonacci.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---


### Exercici: Algorisme de Fibonacci

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


Video de 8' amb la introducció al càlcul del cost computacional d'un algorisme.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---

### Exercicis

+ Escriu un algorisme que divideixi (ens retorni el quocient de) dos nombres enters, positius i més grans que 1, sense fer servir els operadors de multiplicació `*`, divisió `/` ni mòdul `%`: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb )

+ Contesta les següents preguntes:
  + Quantes operacions (assignacions, comparacions, sumes i restes) fa quan calcula `90/10`?



```python
def divide(dividend, divisor):  
    quotient = 0
    while (dividend >= divisor):  
        dividend -= divisor 
        quotient += 1
    return  quotient 
```

---
### Video: La notació Gran O


Video de 10' amb una introducció a la notació Gran O

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---



### Material addicional. 



És important familiaritzar-se amb les magnituds dels nombres per entendre quan és viable que un ordinador calculi alguna cosa. 

Aquest video, us pot ajudar a tenir una idea intuitiva de la magnitud de les potències de 10. 

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/0fKBhvDjuy0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

