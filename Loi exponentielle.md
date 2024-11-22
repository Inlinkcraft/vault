---
name: Loi exponentielle
type: Matière
---
#STT-2920 

La [[Loi exponentielle]] est l'équivalent continue de la [[Loi géométrique|loi géométrique]].

$$X \sim \text{Exponentiel}(\lambda) \qquad X \sim \mathcal{E}(\lambda)$$

> [!Info]
> $X$: suit une [[Loi géométrique|loi géométrique]] continue

### Definition
---
###### [[Fonction de densité]]:
$$f_{X}(k) = \mathbb{P}[X = k] = 
\begin{cases}
\lambda e^{-\lambda x} & \text{si } x > 0 \\
0 & \text{sinon}
\end{cases}
$$

###### [[Espérance]]:
$$\mathbb{E}[X] = \frac{1}{\lambda}$$

###### [[Fonction de répartition]]:
$$F(x) = \begin{cases}
0 & \text{si } x \le 0 \\
(1-e^{-\lambda t}) & \text{si } x > 0 \\
\end{cases}
$$

### Un processus limite de la loi géométrique
---
![[STT-2920-Chapter-7.pdf#page=7&rect=25,195,359,233&color=red|STT-2920-Chapter-7, p.7]]

Supposons un processus de [[Loi de Bernoulli|Bernoulli]] avec probabilité $p$ de succès à chaque épreuve. Supposons de plus que cela prend $\Delta t$ secondes pour réaliser chacune des épreuves. 
 - On peut voir $p$ comme le taux de succès par épreuve. 
 - Soit $\lambda = p \delta t$ le taux de succès par seconde. 
 - Soit $Y$ : Le nombre d’épreuves nécessaires pour obtenir le premier succès. 
 - Soit $T$ : le temps (disons en secondes) nécessaire pris pour obtenir le premier $s$
Pour $t > 0$, la fonction de répartition de $T$ est:
$$F_{T}(t)=\mathbb{P}\left[T\leq t\right]=\mathbb{P}\left[Y\Delta t\leq t\right]=\mathbb{P}\left[Y\leq{\frac{t}{\Delta t}}\right]=1-(1-p)^{t/\Delta t}=1-(1-\lambda\Delta t)^{t/\Delta t}$$
Si on fait la limite de cette fonction de répartition lorsque $\Delta t → 0$, on obtient
$$\begin{array}{r}{{F_{T}^{*}(t)=\displaystyle\operatorname*{lim}_{\Delta t\to0}F_{T}(t)=\operatorname*{lim}_{\Delta t\to0}\left[1-\left(1-\lambda\Delta t\right)^{t/\Delta t}\right]=1-\operatorname*{lim}_{\Delta t\to0}\left[\left(1-\lambda\Delta t\right)^{1/\Delta t}\right]^{t}}}\\ {{=1-\left[\operatorname*{lim}_{\Delta t\to0}\left(1-\lambda\Delta t\right)^{1/\Delta t}\right]^{t}=1-\left[\mathrm{e}^{-\lambda t}\right]^{t}=1-\mathrm{e}^{-\lambda t}}}\end{array}$$
La fonction de densité associée est:
$$f_{T}^{*}(t)={\frac{\mathrm{d}}{\mathrm{d}t}}\left[F_{T}^{*}(t)\right]={\frac{\mathrm{d}}{\mathrm{d}t}}\left[1-\mathrm{e}^{-\lambda t}\right]=\lambda\mathrm{e}^{-\lambda t}$$
On reconnaît la loi exponentielle de paramètre $\lambda$ ! ! ! 