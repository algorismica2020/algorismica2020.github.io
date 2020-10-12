# Sessió en línia del dia 13/10/2020: Introducció a l'algorísmica

Es recomana seguir aquests continguts en el mateix ordre que apareixen en aquesta pàgina.

Els apunts complets d'aquest tema es poden veure [aquí](https://algorismica2020.github.io/slides/introduccio.html). 

> **AVÍS**: Recordeu que si voleu conservar els notebooks que obriu des d'aquesta pàgina heu de baixar-los al vostre ordinador abans de tancar Colab.


---

### Video: Quin és l'origen de la paraula "algorisme"?

Video de 3' sobre l'origen de la paraula "algorisme". 

<center>
<iframe src="https://www.bbc.co.uk/ideas/videos/why-algorithms-are-called-algorithms/p07gdlwf/player" width="500" height="440" scrolling="no" style="overflow: hidden" allowfullscreen frameborder="0"></iframe>
</center>

---

### Video: Què és un algorisme?

Video de 8' sobre la definició del concepte d'algorisme, sobre la diferència entre un algorisme i un programa. Diferents algorismes per calcular l'arrel quadrada.

<center>
<iframe src="https://drive.google.com/file/d/1M089dhy23Jby5lBCHHE2UxNz-V1_Qdkp/preview" width="640" height="480"></iframe>
</center>


---

### Video: Quines propietats han de tenir els bons algorismes?

Video de 13' sobre  la correcció i eficiència d'un algorisme. El cas del problema del viatjant de comerç.

<center>
<iframe src="https://drive.google.com/file/d/1lXjUGQZq9C9koIfQZ9MwW4OkofGnzoQb/preview" width="640" height="480"></iframe>
</center>
--- 

### Elegància

Un algorisme és elegant si és fàcil de llegir. Deia D.Knuth, un dels pares de l’algorísmica, que els algorismes son quelcom destinat a ser llegit per humans i nomes esporàdicament executats per ordinadors.

En general, direm que un algorisme es elegant si es segueixen les seguents pautes:

+ El codi està ben estructurat a nivell de blocs i de funcions.
+ El codi és minimal: no hi sobra ni hi falta res.
+ Els noms de les variables i funcions es informatiu i ajuda a entendre l’algorisme.
+ El codi fa servir el tipus de variables i les col·leccions mes adients al problema.
+ Es fàcil comprovar la correccio del codi.
+ El codi implementa solucions genèriques i les adapta, i no funcions molt específiques que dificulten la seva comprensio.

---

### Tests

Al video s'ha comentat que demostrar la correcció d'un algorisme és difícil en molts casos i queda fora de l'abast d'aquest curs. Hi ha però una solució parcial per aquest problema: podem dir amb tota seguretat que un algorísme és **incorrecte** si per alguna de les seves entrades la sortida és incorrecte. És a dir, **només cal trobar un cas de mal funcionament** per a poder dir que **no és correcte**.

Això ens indica que una de les tasques importants quan escribim un algorisme és pensar un conjunt de casos de test prou ampli i representatiu que ens ajudi a verificar la correcció d'un algorisme. Donat aquest conjunt de casos, ens podem trobar en tres situacions:
+ Algun dels casos genera una sortida incorrecta: llavors podem afirmar de forma segura que l'algorisme no és correcte.
+ Tots els casos generen una sortida correcte: llavors no podem afirmar que l'algorisme és correcte ni incorrecte.

Si usem adequadament la instrucció `assert` de Python pot ser que puguem detectar algorismes incorrectes!

---

### Exercici

Llageix el següent programa, que calcula la mitja de la següent suma: `1+2+3+4+...+999+1000`. 

```python
def main():
    sum = 0.0
    for i in range(1,1001):
        sum += i
    return sum/1000

assert main() == 500.0
 ```

Si l'executem, la instrucció `assert` genera un error.
+ És incorrecte l'algorisme?
+ Saps perquè genera l'error?

---

### Video: Com expressem els algorismes?

Video de 10' sobre els algorismes i els llenguatges de programació.

<center>
<iframe src="https://drive.google.com/file/d/1X_bCfNFOcu1Lk7nqIog4KaKhm3yFx4Bn/preview" width="640" height="480"></iframe>
</center>

---
