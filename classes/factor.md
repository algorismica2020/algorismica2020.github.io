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
