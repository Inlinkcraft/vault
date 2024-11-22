---
name: Problème d'urne et boule
type: Matière
---
#STT-2920


Le problème d'urne et boule est un problème très fréquent dans le monde des probabilité qui fait ressortir différente propriété intéressante.

>[!Info]
>Dans ce type de problème $k$ est le nombre d'urne et $n$ le nombre de boule. De plus, les urne sont toujours distinguable tendis que les boule peuvent être distinguable ou non.

### Boule distinguable
---
Dans le cas ou les boule sont distinguable nous nous retrouvons dans le cas de base du [[Principe fondamental du dénombrement|dénombrement]].
$$k^n$$

### Boule indistinguable
Dans le cas ou les boule sont indistinguable nous faisons usage de symbole et d'emplacement. En d'autre mots nous posons:
- $n$ boule
- $k - 1$ séparateur (car il a $k$ urne)
- Donc un total de $n + k - 1$ symbole et emplacement
Alors
$${n + k - 1 \choose k - 1} \qquad  \text{Équivalent} \qquad {n + k - 1 \choose n}$$

#### Aux moins 1 boule dans chaque urne
Le problème est similaire aux précédent à l'exception que nous "cachons" une boule dans chaque urne.
1. Placer 1 boule dans chaque urne. Il a juste 1 façons de faire cela ce qui nous laisse un total de $n-k$ boule.
2. Distribuer les boule restante dans les urne comme d'habitude.
$$(1) \cdot {(n-k) + (k - 1) \choose k -1} \qquad \text{Équivalent} \qquad {n - 1 \choose k - 1}$$