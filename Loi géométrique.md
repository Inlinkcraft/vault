---
name: Loi géométrique
type: Matière
---
#STT-2920 

La loi géométrique est la une suite de [[Loi de Bernoulli|lois de Bernoulli]] jusqu'à obtenir le premier succès

$$X \sim \text{Géométrique}(p) \qquad X \sim \text{G}(p)$$

> [!Info]
> $X$: Le nombre d'épreuve avant le premier succès

### Definition
---
###### [[Fonction de masse]]:
$$p_{X}(k) = \mathbb{P}[X = k] = 
\begin{cases}
(1-p)^{k-1}p & \text{si } k \in \{0, 1, 2, \dots, n\} \\
0 & \text{si non}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = \frac{1}{p}$$

###### [[Fonction de répartition]]:
$$F(x) = \begin{cases}
0 & \text{si } x \le 0 \\
1-(1-p)^{\lfloor x \rfloor} & \text{si } x > 0
\end{cases}
$$

### Propriété de perte de mémoire
---
Pour $Y \sim \text{géométrique}(p)$ et $t, s \in \mathbb{Z}_+$ :
$$
P[Y > t + s | Y > s] = P[Y > t]
$$

>[!Info] Interprétation
>Dans un processus de [[Loi de Bernoulli|Bernoulli]], si on a déjà écoulé $s$ épreuves sans succès, la probabilité d’écoulé $t$ épreuves supplémentaires sans succès est la même que la probabilité d’écoulé $t$ |épreuves sans succès depuis le début du processus. 

>[!Attention] Remarque
>Lorsqu’une [[Variable aléatoire|v.a]]. respecte $P[Y > t + s | Y > s] = P[Y > t]$, on dit qu’elle possède la propriété de perte de mémoire. La loi géométrique est la seule loi [[Cas discret|discrète]] possédant la propriété de perte de mémoire.

([[STT-2920-Chapter-7.pdf#page=6&selection=0,51,257,85&color=yellow|STT-2920-Chapter-7, p.6]])