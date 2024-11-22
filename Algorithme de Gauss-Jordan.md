---
name: Algorithme de Gauss-Jordan
type: Matière
---
#MAT-2930 

Algorithme de Gauss-Jordan consiste a effectuer les même étape que dans l'[[Élimination de Gauss|élimination de Gauss]], mais de continuer afin d'avoir les pivot égale à un et des zero aux dessus de ceux-ci.
### But
---
Le but de la résolution est de simplifier d'avantage une [[Matrice|matrice]] afin d'obtenir cette forme:
$$\left[ 
\begin{array}{cccc|c}
1 & 0 & \dots & 0 & x \\
0 & 1 & \dots & 0 & x\\
\vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & \dots & 1 & x\\ 
\end{array}
\right]$$
Il est facile de voir à ce moment la valeur de chacune des variable
### Résolution
---
#### Manipulations
- Le pivot doit être égale à 1
- Il est possible de déplacer une ligne (interchanger avec une autre)
- Il est possible de multiplier une ligne par un scalaire
- Il est possible de faire une [[Vecteur#Combinaison Linéaire|combinaison linéaire]] entre deux lignes.

#### Exemple
soit la [[Matrice|matrice]] échelonné suivante:
$$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & 2 & 1 & 2 \\
\colorbox{red}{0} & \colorbox{green}{2} & -2 & 6\\
\colorbox{red}{0} & \colorbox{red}{0} & \colorbox{green}{5} & -10\\ 
\end{array}
\right]$$

1. Nous ajustement de tous pivot pour que ceux-ci soit égale à 1
    1. $l_{2} \leftarrow l_2/2$
    2. $l_{3} \leftarrow l_3/5$
    3. $$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & 2 & 1 & 2 \\
\colorbox{red}{0} & \colorbox{green}{1} & -1 & 3\\
\colorbox{red}{0} & \colorbox{red}{0} & \colorbox{green}{1} & -2\\ 
\end{array}
\right]$$

2. Retirons alors la valeur aux dessus du deuxième pivot
    1. $l_{1} \leftarrow l_{1} - 2l_{2}$
    2. $$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & \colorbox{red}{0} & 3 & -4 \\
\colorbox{red}{0} & \colorbox{green}{1} & -1 & 3\\
\colorbox{red}{0} & \colorbox{red}{0} & \colorbox{green}{1} & -2\\ 
\end{array}
\right]$$

2. Retirons alors les valeurs aux dessus du troisième pivot
    1. $l_{1} \leftarrow l_{1} - 3l_{3}$
    2. $l_{2} \leftarrow l_{2} + l_{1}$
    3. $$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & \colorbox{red}{0} & \colorbox{red}{0} & 2 \\
\colorbox{red}{0} & \colorbox{green}{1} & \colorbox{red}{0} & 1\\
\colorbox{red}{0} & \colorbox{red}{0} & \colorbox{green}{1} & -2\\ 
\end{array}
\right]$$

4. Nous obtenons alors la matrice échelons réduite. Ici il est facile de voir sans substitution les valeurs de chacune des variable pour la solutions.

> [!Attention]
> Dans une matrice qui n'est pas carré un pivots ne peut pas être zero donc:
>  $$\left[ \begin{array}{cccc|c} \colorbox{green}{1} & -1 & \colorbox{red}{0} & 2 & 1 \\ \colorbox{red}{0} & 0 &\colorbox{green}{1} & -2 & 1\\ \colorbox{red}{0} & \colorbox{darkorange}{0} & \colorbox{red}{0} & \colorbox{darkorange}{0} & \colorbox{darkorange}{0}\\ \end{array} \right] $$
> Ici la [[Matrice|matrice]] à 2 pivot pour 4 variable donc se système d'équation à une infinité de solution. Ici la [[Matrice|matrice]] à une infinité de solution en 4 dimension comme: $[1, 0, 1, 0]$ est une solution valide. 
