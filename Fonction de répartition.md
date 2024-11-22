---
name: Fonction de répartition
type: Matière
---
#STT-2920 

Une fonction de repartions est le cumulatif de tous les probabilité d'une [[Variable aléatoire|variable aléatoire]] jusqu'à une valeur donné $x$.

### Définition mathématique
---
En supposant une [[Variable aléatoire|variable aléatoire]] $X$:
$$F(x) = \mathbb{P}[X \le x]$$

#### Lien avec la fonction de masse
Il existe un lien entre la [[Fonction de masse|fonction de masse]] et la fonction de répartition:
$$F(x) = \sum_{t \le x}p(t)$$

#### Lien avec la fonction de densité
Il existe un lien entre la [[Fonction de densité|fonction de densité]] et la fonction de répartition:
$$F(x) = \int_{-\infty}^{t}f(t) \ dt$$
$$f(x) = \frac{d}{dt}[F(x)]$$

> [!Info]
> Pour calculer une intervalle il est possible d'utilisé la fonction de répartition comme suit:
> $$\mathbb{P}[a \le X \le b] = F(b) - F(a)$$
> $$\mathbb{P}[X \gt b] = 1 - F(b)$$
