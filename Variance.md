---
name: Variance
type: Matière
---
#STT-2920 

La [[Variance|variance]] évalue a qu'elle point on s'attend que la valeur obtenue ai un $\pm$ grand écart avec la [[Espérance|espérance]].

### Définition mathématique
---
$$\sigma_{X}^{2} = \mathbb{V}\text{ar}[X] = \mathbb{E}[(X - \mu_{X})^{2}] = \begin{cases}
\sum_{x\in\mathbb{R}}(x - \mu_{X})^{2}p_{X}(x) & \text{Dans le cas discret} \\
\int_{\mathbb{R}}(x - \mu_{X})^{2} f_{X}(x) \ dx & \text{Dans le cas continue} \\
\end{cases}$$

#### Écart type
L'écart-type est donné par
$$\sigma_{X} = \sqrt{\mathbb{V}\text{ar}[X]}$$


### Propriété
---
- $\mathbb{V}\text{ar}[X] = \mathbb{E}[X^{2}]-\mathbb{E}[X]^2$
- $\mathbb{V}\text{ar}[b] = 0$
- $\mathbb{V}\text{ar}[aX + b] = a^2\mathbb{V}\text{ar}[X]$
- $\mathbb{V}\text{ar}[X+Y]=\mathbb{V}\text{ar}[X] + \mathbb{V}\text{ar}[Y]$ si $X$ et $Y$ sont [[Indépendance probabiliste|indépendant]]

>[!Info]
>Pour calculer la variance l'équation $\mathbb{V}\text{ar}[X] = \mathbb{E}[X^{2}]-\mathbb{E}[X]^2$ est très utile. 