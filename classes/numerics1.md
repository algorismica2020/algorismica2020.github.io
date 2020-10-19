# Sessió en línia del dia 19/10/2020: Algorismes Numèrics I

Aquesta sessió té una durada aproximada de 60 minuts i està formada per alguns videos sobre els aspectes teòrics del tema i diversos exercicis. 
Es recomana seguir aquests continguts en el mateix ordre que apareixen en aquesta pàgina.

Els apunts complets d'aquest tema es poden veure [aquí](https://algorismica2020.github.io/slides/numerics1.html). 

> **AVÍS**: Recordeu que si voleu conservar els notebooks que obriu des d'aquesta pàgina heu de baixar-los al vostre ordinador abans de tancar Colab.


---

### Video: Introducció als sistemes de numeració.

Video de 9' sobre l'història dels sistemes de numeració, la seva relació amb les operacions aritmètiques i el concepte de base de representació.

<center>
<iframe src="https://drive.google.com/file/d/1cWEOLgZx3O7-Ip9mc38EYoBiqNZGZg1z/preview" width="640" height="480"></iframe>
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

