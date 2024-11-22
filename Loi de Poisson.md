---
name: Loi de Poisson
type: Matière
---
#STT-2920 

Une [[Variable aléatoire|variable aléatoire]] peut suivre une loi de Poisson d'un paramètre donné $\nu$

$$X \sim \text{Poisson}(\nu) \qquad X \sim \mathcal{P}(\nu)$$

> [!Info]
> $X$: suit la loi de Poisson de moyenne $\nu$.

### Definition
---
###### [[Fonction de masse]]:
$$p_{X}(k) = \mathbb{P}[X = k] = 
\begin{cases}
e^{-\nu}\frac{\nu^{k}}{k!} & \text{si } k \in \{0, 1, 2, \dots\} \\
0 & \text{sinon}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = \nu$$

###### [[Fonction de répartition]]:
#TODO 

### Comme la limite d’une loi binomiale
---
Supposons qu’un phénomène relativement rare se produit en moyenne $λ$ fois par unité de temps. 
Subdivisons l’unité de temps en $n$ sous-intervalles. En moyenne, le phénomène devrait se produire dans un tel sous-intervalle $λ/n$ fois. 
On interprète chaque sous-intervalle de temps comme une épreuve de [[Loi de Bernoulli|Bernoulli]] de probabilité $pn = λ/n$, et le nombre de fois $N$ qu’on observe le phénomène dans notre unité de temps est alors une $\text{binomiale}(n, λ/n)$. Ainsi, pour:
$$\begin{array}{r}{\mathbb{P}\left[N=k\right]={\binom{n}{k}}{\left({\frac{\lambda}{n}}\right)}^{k}{\Big(}1-{\frac{\lambda}{n}}{\Big)}^{n-k}}\\ {={\frac{n(n-1)\cdots\left(n-k+1\right)}{k!}}{\frac{\lambda^{k}}{n^{k}}}{\Big(}1-{\frac{\lambda}{n}}{\Big)}^{k}}\\ {={\frac{n(n-1)\cdots\left(n-k+1\right)}{n^{k}}}{\frac{\lambda^{k}}{k!}}{\Big(}1-{\frac{\lambda}{n}}{\Big)}^{k}}\\ {\approx{\frac{\lambda^{k}}{k!}}e^{-\lambda}}\end{array}$$
On reconnaît la loi de Poisson de paramètre $\lambda$! ! !.