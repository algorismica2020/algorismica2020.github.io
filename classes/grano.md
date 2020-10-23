## Exercicis sobre complexitat algorísmica.

1. Un algorisme d'ordenació de llistes te una complexitat `O(n log n)` per ordenar una llista de `n` elements. Si triga 1ms en ordenar 1000 elements, quant trigarà en ordenar-ne 1000000?

<!--- (Resposta: 2000ms, atès que podem fer la regla de 3 següent: si en el cas (10^3 log 10^3) triga 10^3 , en el cas (10^6 log 10^6) trigarà x . Aillant x resulta 2000.) --->

2. Quina és la complexitat `O()`d'aquests algorismes?
+ `5+0.0001n^3 + 0.025n`
+ `500n + 100n^1.5 + 50n log n`
+ `0.3n + 5n^1.5 + 2.5 n^1.75`
+ `0.01 n log n + n (log n)^2`

<!--- (Resposta: n^3, n^1.5, n^1.75, n (log n)^) --->

3. Dos algorismes `A` i `B` tenen una complexitat  `O(0.1 n^2 log n)` i `O(2.5 n^2)`, respectivament, per un problema de mida `n`. 
Si el problema que vols resoldre sempre tindrà una mida `n < 10^9`, quin escolliries?
<!--- Resposta: L'algorisme A, atès que 0.1 * 10**9**2 * math.log(10**9) és menor que 2.5 *
10*9*2 --->



