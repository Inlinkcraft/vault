---
name: Transformation de variable aléatoire
type: Matière
---
Dans le cas où on pose une [[Variable aléatoire|variable aléatoire]] en fonction d'une autre [[Variable aléatoire|variable aléatoire]], il s'agit d'une |transformation de variable aléatoire:
$$Y = g(X)$$

### Résolution exemple
---
On à la densité de $X$ soit:
$$f_{X}(x) = \begin{cases}
2e^{-2x} & \text{si } x > 0 \\
0 & \text{si } x \le 0
\end{cases}
\qquad
Y = \sqrt{X}
$$
Ici on cherche la $f_{Y}(y)$ pour ce faire nous allons premièrement trouver $F_{Y}(y)$
$$
\begin{array}{rcll}
F_{Y}(y) &=& \mathbb{P}[Y \le y] &\\
&=& \mathbb{P}[\sqrt{X} \le y] & \text{car } Y = \sqrt{X}\\
&=& \mathbb{P}[X \le y^{2}] & \\
&=& \int_{0}^{y^{2}}f_{X}(x) \ dx & \\
&=& 1-e^{-2y^2} & \\
\end{array}
$$
Pour trouver $f_{Y}(y)$ on dérive $F_{Y}(y)$ donc:
$$
\begin{array}{rcll}
f_{Y}(y) &=& \frac{d}{dy}(1-e^{-2y^2}) &\\
 &=& 4ye^{-2y^2} &\\
\end{array}
$$