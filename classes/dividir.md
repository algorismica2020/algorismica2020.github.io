# Sessió en línia del dia 30/11/2020: Dividir i Vèncer

Es recomana seguir aquests continguts en el mateix ordre que apareixen en aquesta pàgina.

Els apunts complets d'aquest tema es poden veure [aquí](https://algorismica2020.github.io/slides/dividir.html). 

> **AVÍS**: Recordeu que si voleu conservar els notebooks que obriu des d'aquesta pàgina heu de baixar-los al vostre ordinador abans de tancar Colab.


---

> En la cultura popular, divideix i venceràs fa referència a un refrany que implica resoldre un problema difícil, dividint-lo en parts més simples tantes vegades com sigui necessari, fins que la resolució de les parts es torna òbvia i senzilla. La solució del problema principal es construeix amb les solucions de les parts en que s'ha dividit el problema.

> En el camp de les ciències de la computació, el terme divideix i venceràs (DiV) fa referència a un dels paradigmes més importants de disseny algorítmic. El mètode es basa en la resolució recursiva d'un problema dividint-lo en dos o més subproblemes d'igual tipus o similar. El procés continua fins que els subproblemes arriben a ser prou senzills perquè es resolguin directament. Al final, les solucions a cadascun dels subproblemes es combinen per donar la solució del problema original.

> Font: https://ca.wikipedia.org/wiki/Algorisme_divideix_i_vencer%C3%A0s

### Video: Introducció

Video de 10' sobre l'estratègia de D&V.

<iframe src="https://drive.google.com/file/d/15MczHDPJgylXbh1p5K5UkUthgu0gRyTZ/preview" width="640" height="480"></iframe>

### Com resoldre un problema amb aquesta estratègia?

Les qüestions a resoldre són tres:
+ Com anem dividint el problema, de forma recursiva, en subproblemes?
+ Com aturem la recursió i donem una solució al darrer subproblema?
+ Com combinem les solucions recursives per assolir la solució del problema complet?

Una possible solució pel problema de la suma dels elements d'una llista seria:

```python
def sum(l):
   if len(l) == 1:
        return l[0]
   else:
        return l[0] + sum(l[1:])
```

Aquest és un algorisme **correcte** (retorna el nombre corresponent a la suma dels elements de la llista), que ha respost a les tres preguntes de la següent manera:

+ La divisió del problema és en dues subllistes, la primera formada per 1 elements i la segona formada per la resta d'elements.
+ La recursió s'atura quan hi ha un únic element a la llista, que és retornat.
+ La solució s'obté al anar sumants els elements individuals a la solució recursiva de la resta de la llista.

És eficient aquest algorisme? Fem `n` operacions de suma, pel que no guanyem res respecte a la solució *ingènua* del problema.

### Com calcular la complexitat d'un algorisme que implementa l'estratègia de D&C

Video de 7' sobre el Teorema Màster.

<iframe src="https://drive.google.com/file/d/1pL0jhQIID0wUYWrK7DOYbvcEF5Uun3_1/preview" width="640" height="480"></iframe>

### Exercici

Calculeu la complexitat d'una sèrie d'algorismes que tenen aquestes relacions de recurrència:

+ `3 T(n/2) + n^2`
+ `4 T(n/2) + n^2`
+ `2 T(n/4) + n^0.51`
+ `3 T(n/2) + n`

### Video: Algorisme Mergesort

Video de 10' sobre l'algorisme MergeSort, un algorisme d'ordenació de llites amb complexitat `O(n log n)`.

<iframe src="https://drive.google.com/file/d/1jVpXCr1VVunRujjsJyzwnsXQHC5FFMmc/preview" width="640" height="480"></iframe>





