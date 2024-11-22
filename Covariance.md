---
name: Covariance
type: Matière
---
#STT-2920 

La covariance donne comment une variable varie par rapport a une autre. Observable plus facilement avec le [[Coefficient de corrélation|coefficient de corrélation]].

### Definition
---
La covariance de $X$ et $Y$ :
$$ \text{Cov}[X, Y] = E[(X - \mu_X)(Y - \mu_Y)] $$
Elle est positive si $X$ et $Y$ augmentent ensemble, négative dans le cas contraire.

### Propriétés de la covariance
---
Pour tout [[Vecteur aléatoire|vecteur aléatoire]] $(X, Y)$ et pour $a, b, c, d \in \mathbb{R}$, on a :

1. $\text{Cov}[X, Y] = E[XY] - E[X]E[Y]$
2. $\text{Var}[X + Y] = \text{Var}[X] + 2\text{Cov}[X, Y] + \text{Var}[Y]$
3. $\text{Cov}[aX + b, cY + d] = ac \, \text{Cov}[X, Y]$

Si $X$ et $Y$ sont [[Indépendance probabiliste|indépendantes]], alors :
1. $\text{Cov}[X, Y] = 0$
2. $\text{Var}[X + Y] = \text{Var}[X] + \text{Var}[Y]$