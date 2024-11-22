---
name: Impédance
type: Matière
---
#GEL-1000 

L'[[Impédance|impédance]] est une [[Modélisation|modelisation]] plus approprier d'une [[Composante électrique|composante]] qui met en relation l'exitation et la réponse.

## Modèle mathématique
---
$$v = Zi \qquad \text{AKA} \qquad v = (R+X(s)) \, i$$
- $R$ est la [[Résistance électrique|résistance]]
- $X(s)$ est la réactance, soit la variation de la réaction dans le temps.

> [!info] Propriété
> La réactance inductive est alors décrite comme: $v = L\frac{di}{dt} \ \text{ou} \ v = Ls$
> La réactance capacitive est alors décrite comme $i = C \frac{dv}{dt} \ \text{ou} \ v = \frac{1}{C}\int i \ dt \ \text{ou} \ v = \frac{1}{Cs}$