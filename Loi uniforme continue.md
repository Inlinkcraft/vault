---
name: Loi uniforme continue
type: Matière
---
#STT-2920 

La [[Loi uniforme continue|loi uniforme continue]] exprime que la probabilité d'une valeurs est uniforme sur une intervalle donnée.

$$X \sim \text{Uniforme}([a, b]) \qquad X \sim \mathcal{U}([a, b])$$

> [!Info]
> $X$: est uniforme

### Definition
---
###### [[Fonction de densité]]:
$$f_{X}(k) = \mathbb{P}[X = k] = 
\begin{cases}
\frac{1}{b-a} & \text{si } a < x < b \\
0 & \text{sinon}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = \frac{a+b}{2}$$

###### [[Fonction de répartition]]:
$$F(x) = \begin{cases}
0 & \text{si } x \le a \\
\frac{x-a}{b-a} & \text{si } a < x < b \\
1 & \text{si } x \ge b \\
\end{cases}
$$

### Loi uniforme continue sur une région de $\mathbb{R}^2$
Soit $E \subset \mathbb{R}^2$, on dit que le couple $(X, Y)$ suit la loi uniforme sur $E$ si $\mathbb{P}[(X, Y) \in E] = 1$ et que tout $B \subset E$, on a que:
$$\mathbb{P}[(X, Y) \in B] = \frac{\text{Aire de } B}{\text{Aire de } E}$$
$$f(x, y) = \begin{cases}
\frac{1}{\text{Aire de } E} & \text{si } (x, y) \in E \\ \\
0 & \text{sinon}
\end{cases}$$
