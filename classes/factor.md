# Factorització ingènua.

L'algorisme més simple per factoritzar és:

```python
import math 

def primeFactors(n): 
    # Impremeix el nombre de 2 que divideixen n 
    while n % 2 == 0: 
        print(2) 
        n = n / 2
    # n és senar! 
    # anem saltant de 2 en 2 ( i = i + 2)  
    for i in range(3, int(math.sqrt(n))+1, 2): 
        # mentre i divideix n, imprimim i i dividim n 
        while n % i == 0: 
            print(i) 
            n = n / i 
    # Imprimim el primer si és més gran que 2 
    if n > 2: 
        print(n)
  ```

### Com funciona?
+ Primer, mirem quantes vegades és divisible per 2. Un cop ho hem trobat, l'hem reduït a un nombre senar.
+ Llavors anem comprovant si és divisible per cada possible sombre senar que és menor que `sqrt(n)`. 

### Perquè ho fem fins `sqrt(n)`?
Ho podem veure a partir de dues observacions:

> Si un nombre `n` no és primer, al menys un dels seus factors és menor que `sqrt(n)`

Suposem que `n` és un nombre enter positiu tal que `n=pq`, on `p` i `q` són primers. Assumim `p > sqrt(n)` i `q > sqrt(n)`.  Si multipliquem aquestes dues expressions tenim
`p*q > sqrt(n)*sqrt(n)`, el que implica que `p*q < n`, que és una contradicció. Per tant, `p <= sqrt(n}` o `q <= sqrt(n)`.

> Si un nombre `n` no és primer, hi ha com a màxim un factor més gran que `sqrt(n)`. 

Si existissin dos primers més grans, el seu producte seria més gran que 'n'!
If possible let there exists two greater sqrt(n) then their product sho
