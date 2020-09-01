# Sessió en línia del dia 5/10/2020
---
name:sistnum

## Sobre la representació dels nombres.

Video de 6' amb l'explicació de les transparències 3, 4, 5 i 6.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>

---


#### <p style="background-color: #f18973;">Treball Personal Asíncron</p>

## Bases i Nombres

Fes els següents exercicis:

+ Canvi de base:
  + Pensa com seria l'algorisme que passa un nombre escrit en base 10 a base `a`, on `a` és un nombre enter positiu qualsevol. 
  + Codifica aquest algorisme en Python: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb ) 
  + Comprova que l'algorisme és correcte fent servir aquest recurs: https://www.rapidtables.com/convert/number/base-converter.html
+ Quin és el nombre enter més gran que puc representar usant 64 dígits en base 2?
+ Quin és el nombre enter més gran que puc representar usant 32 dígits en base 16?
---

## Fibonacci.

Video de 6' amb l'explicació de Fibonacci.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---
#### <p style="background-color: #f18973;">Treball Personal Asíncron</p>



+ Copia l'algorisme recursiu de Fibonacci i calcula el terme 10 i el terme 100: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb ) 
+ Què ha passat quan has intentat calcular el terme 100? 


---


## Recursivitat.

Video de 6' amb l'explicació de la recursivitat.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---


## Altres versions de Fibonacci.

Video de 6' amb l'explicació amb llistes.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---

#### <p style="background-color: #f18973;">Treball Personal Asíncron</p>

## Algorisme de Fibonacci

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

## **Passos computacionals** d'un algorisme?


Video de 8' amb l'explicació.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---

#### <p style="background-color: #f18973;">Treball Personal Asíncron</p>

+ Escriu un algorisme que divideixi (ens retorni el quocient de) dos nombres enters, positius i més grans que 1, sense fer servir els operadors de multiplicació `*`, divisió `/` ni mòdul `%`: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/notebooks/empty.ipynb )

+ Contesta les següents preguntes:
  + Quantes operacions (assignacions, comparacions, sumes i restes) fa quan calcula `90/10`?

#### <p style="background-color: #33FFCE;">Solució</p>

```python
def divide(dividend, divisor):  
    quotient = 0
    while (dividend >= divisor):  
        dividend -= divisor 
        quotient += 1
    return  quotient 
```

---
## La notació Gran O


Video de 10' amb l'explicació.

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>


---

#### <p style="background-color: #f18973;">Treball Personal Asíncron</p>

## Magnitud dels nombres. 



És important familiaritzar-se amb les magnituds dels nombres per entendre quan és viable que un ordinador calculi alguna cosa. 

Aquest video, us pot ajudar a tenir una idea intuitiva de la magnitud de les potències de 10. 

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/0fKBhvDjuy0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

