---
name: Loi de Bernoulli
type: Matière
---
#STT-2920 

La [[Loi de Bernoulli|loi de Bernoulli]] met en relation le principe de succès et échec de façons à ce que la [[Variable aléatoire|variable aléatoire]] puisse seulement prendre les valeur $1$ ou $0$.

$$X \sim \text{Bernoulli}(p)$$

> [!Info]
> $X$: est réussi ou non.

Une épreuve de Bernoulli est lorsque nous procédons a la succession de plusieurs [[Expérience aléatoire|expérience aléatoire]] avec la loi de Bernoulli.  L'épreuve de Bernoulli à sont analogue: [[Loi binomiale]].
### Definition
---
###### [[Fonction de masse]]:
$$p_{X}(x) = \mathbb{P}[X = x] = 
\begin{cases}
p & \text{si } x = 1 \\
1-p & \text{si } x = 0 \\
0 & \text{si } x \notin \{0, 1\}
\end{cases}
$$
$$p_{X}(x) = \mathbb{P}[X = x] = 
\begin{cases}
p^{x}(1-p)^{1-x} & \text{si } x \in \{0, 1\} \\
0 & \text{sinon}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = p$$

###### [[Fonction de répartition]]:
#TODO 