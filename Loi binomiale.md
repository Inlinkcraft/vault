---
name: Loi binomiale
type: Matière
---
#STT-2920 

La loi binomial est qui effectue une succession de [[Loi de Bernoulli|lois de Bernoulli]] [[Indépendance probabiliste|indépendamment]].

$$X \sim \text{Binomial}(p) \qquad X \sim \mathcal{B}(p)$$

> [!Info]
> $X$: Le nombre de succès en $n$ épreuve

### Definition
---
###### [[Fonction de masse]]:
$$p_{X}(k) = \mathbb{P}[X = k] = 
\begin{cases}
{n \choose k}p^k(1-p)^{n-k} & \text{si } k \in \{0, 1, 2, \dots, n\} \\
0 & \text{si non}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = np$$

###### [[Fonction de répartition]]:
#TODO 