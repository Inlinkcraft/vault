---
name: Espérance
type: Matière
---
#STT-2920 

L'[[Espérance|espérance]] d'une [[Variable aléatoire|variable aléatoire]] est ce qu'on espère obtenir en "moyenne" ($\bar{x}$) si nous répétions l'[[Expérience aléatoire|expérience aléatoire]] à l'infinie. Par contre, l'espérance n'est pas égale à la moyenne. De plus, l'espérance peut diverger et tendre vers l'infinie, c'est-a-dire que l'espérance peut ne pas existé.

### Symbolique mathématique
---
L'espérance est noté comme suit:
$$\mathbb{E}[X] \qquad \text{où} \qquad \mu_X$$

### Definition Mathématique
---
La définition mathématique de l'espérance dépend du [[Variable aléatoire#Support|support]] de la [[Variable aléatoire|v.a.]] et de sa [[Fonction de masse|fonction de masse]] ou [[Fonction de densité]]:
$$\text{Discrète:} \qquad \mathbb{E}[X] = \sum_{x\in S_{X}} x p(x) = \sum_{x\in S_{X}} x \mathbb{P}[X = x]$$
$$\text{Continue:} \qquad \mathbb{E}[X] = \int_{S_{X}} x f(x) \ dx = \int_{S_{X}} x \mathbb{P}[X = x] \ dx$$

### Propriété
---
Soient $X$ et $Y$ deux [[Variable aléatoire|variables aléatoires]] dont les espérances sont respectivement $E[X]$ et $E[Y]$ . Soient $a$ et $b \in \mathbb{R}$. Alors:

- $\mathbb{E}[X + Y] = \mathbb{E}[X] + \mathbb{E}[Y]$
- $\mathbb{E}[b] = b$
- $\mathbb{E}[aX] = a\mathbb{E}[X]$
- $\mathbb{E}[g(X)] = \sum_{x \in S_{X}} g(x)\mathbb{P}[X = x] = \sum_{x \in S_{X}}g(x)p_{X}(x)$
-  $\mathbb{E}[g(X)] = \int_{\mathbb{R}} g(x)f_{X}(x) \ dx$
- $\mathbb{E}[g(X, Y)] = \sum_{(x,y) \in \mathbb{R}^{2}} g(x,y)p(x, y)$
-  $\mathbb{E}[g(X, Y)] = \iint_{\mathbb{R}^2} g(x, y)f_{X, Y}(x, y) \ dxdy$

> [!Attention]
> $$\mathbb{E}[X^{2}] \ne \mathbb{E}[X]^{2}$$