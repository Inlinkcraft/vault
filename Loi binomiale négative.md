---
name: Loi binomiale négative
type: Matière
---
#STT-2920 

La loi binomial négative permet de savoir combien d'[[Loi de Bernoulli|lois de Bernoulli]] pour obtenir le $m$-ième succès.

$$X_m \sim \text{Binomial négative}(p) \qquad X_m \sim \text{Bn}(p)$$

> [!Info]
> $X_m$: Le nombre d’épreuves nécessaires pour obtenir le $m$-ième succès.

### Definition
---
###### [[Fonction de masse]]:
$$p_{X_m}(k) = \mathbb{P}[X_m = k] = 
\begin{cases}
{k-1 \choose m-1}p^{m}(1-p)^{k-m} & \text{si } k \in \{m, m+1, 2m+, \dots\} \\
0 & \text{sinon}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = \frac{m}{p}$$

###### [[Fonction de répartition]]:
#TODO 