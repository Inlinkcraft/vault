---
name: Vecteur aléatoire
type: Matière
---
#STT-2920 

Le vecteur aléatoire est un [[Vecteur|vecteur]] composé de [[Variable aléatoire|variable]]. 

### Notation mathématique
---
Un vecteur aléatoire est noté comme suit:
$$\mathbb{X} = (X_{1}, X_{2}, X_{3}, \dots, X_{n})$$

> $X_i$ sont des variable aléatoire
> $n$ est la dimension du vecteur aléatoire

>[!Info]
>Dans le cas où $n = 0$ on noteras le vecteur comme $(X, Y)$ aux lieux de $(X_{1}, X_{2})$

### Calcul de probabilité sur des vecteur aléatoire
---
#### [[Fonction de masse]] conjointe
La [[Fonction de masse|fonction de masse]] conjointe est exprimer comme suit:
$$p(x, y) = \mathbb{P}[X=x, Y=y] \qquad p(x, y) = \mathbb{P}[X=x \cap Y=y]$$
###### Propriété
- $\sum_{(x, y) \in \mathbb{R}^{2}}p(x, y) = 1$
- $\mathbb{P}[(X, Y) \in B] = \sum_{B}p(x, y)$

#### [[Fonction de densité]] conjointe
La [[Fonction de densité|fonction de densité]] conjointe est exprimer comme suit:
$$p(x, y) = \mathbb{P}[(X, Y) \in B] = \iint_{B}f(x, y) \ dxdy$$
###### Propriété
- $f(x, y) \ge 0$ pour tout couple de $(x, y)$
- $\iint_{\mathbb{R}^2}f(x, y) \ dxdy = 1$

### Fonction de répartition d'un vecteur aléatoire
---
La [[Fonction de répartition|fonction de répartition]] d'un [[Vecteur aléatoire|vecteur aléatoire]] est fonctionne de façons similaire a une [[Variable aléatoire|variable aléatoire]] simple:
$$F(x, y) = \mathbb{P}[X \le x, Y \le y]$$
$$F(x, y) = \iint_{\mathbb{R}^{2}f(x, y)}\ dxdy$$
$$f(x, y) = \frac{\partial^2}{\partial y \partial x}[F(x, y)]$$