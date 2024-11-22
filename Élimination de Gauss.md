---
name: 
type: Matière
---
#MAT-2930

L'élimination de Gauss est une méthode permettant de résoudre un système d'équation linéaire a l'aide de [[Matrice|matrice]].

### But
---
Le but de la résolution est d'optenir une matrice de cette forme:
$$\left[ 
\begin{array}{cccc|c}
p & x & \dots & x & x \\
0 & p & \dots & x & x\\
\vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & \dots & p & x\\ 
\end{array}
\right]$$
Pour ensuite résoudre l'équation par substitution.

### Résolution
---
#### Manipulations
- Le pivot ne doit jamais être égale à 0
- Il est possible de déplacer une ligne (interchanger avec une autre)
- Il est possible de multiplier une ligne par un scalaire
- Il est possible de faire une [[Vecteur#Combinaison Linéaire|combinaison linéaire]] entre deux lignes.

#### Exemple
soit la [[Matrice|matrice]] suivante:
$$\left[ 
\begin{array}{ccc|c}
1 & -1 & -1 & 2 \\
3 & -3 & 2 & 16\\
2 & -1 & 1 & 9\\ 
\end{array}
\right]$$

1. Nous déterminons le premier pivot

$$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & -1 & -1 & 2 \\
3 & -3 & 2 & 16\\
2 & -1 & 1 & 9\\ 
\end{array}
\right]$$

> [!Attention]
> Le pivot doit pas être égale à zero

2. Nous effectuons des [[Vecteur#Combinaison Linéaire|combinaison linéaire]] avec la ligne pivot et les ligne inférieur afin d'éliminer toute les valeur inférieur aux pivots.
    1. $l_{2} \leftarrow l_{2} - 3l_1$
    2. $l_{3} \leftarrow l_{3} - 2l_1$
    3. $$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & -1 & -1 & 2 \\
\colorbox{red}{0} & \colorbox{red}{0} & 5 & 10\\
\colorbox{red}{0} & 1 & 3 & 5\\ 
\end{array}
\right]$$

3. Nous sélectionnons le prochain pivot malheureusement celui-ci est un zéros nous allons effectuer une opération pour que celas ne soit pas le cas. 
    1. $$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & -1 & -1 & 2 \\
\colorbox{red}{0} & \colorbox{darkorange}{0} & 5 & 10\\
\colorbox{red}{0} & 1 & 3 & 5\\ 
\end{array}
\right]$$
    2. $l_{3} \leftrightarrow l_1$
    3.  $$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & -1 & -1 & 2 \\
\colorbox{red}{0} & \colorbox{green}{1} & 3 & 5\\ 
\colorbox{red}{0} & \colorbox{red}{0} & \colorbox{green}{5} & 10\\
\end{array}
\right]$$

4. Nous obtenons alors une [[Matrice|matrice]] échelonnée valide qui nous permet de résoudre les équation linéaire par substitution.

### Situation particulière et leur implication
---
#### Équation linéaire à aucune solution
Si lors de la résolution de l'équations la [[Matrice|matrice]] échelonner resemble à:
$$\left[ 
\begin{array}{cc|c}
\colorbox{green}{2} & -1 & 2 \\
\colorbox{red}{0} & \colorbox{green}{-1} & -2 \\ 
\colorbox{red}{0} & \colorbox{red}{0} & \colorbox{darkorange}{-16}\\
\end{array}
\right]$$
le système d'équation a alors aucune solution. En d'autre terme, la dernière ligne du système d'équation peut être interprété comme $0 = -16$ ce qui est impossible.

#### Équation linéaire à infinité de solution
Si lors de la résolution de l'équations la [[Matrice|matrice]] échelonner resemble à:
$$\left[ 
\begin{array}{ccc|c}
\colorbox{green}{1} & 2 & 3 & 4 \\
\colorbox{red}{0} & \colorbox{green}{-2} & -1 & 2 \\ 
\colorbox{darkorange}{0} & \colorbox{darkorange}{0} & \colorbox{darkorange}{0} & \colorbox{darkorange}{0}\\
\end{array}
\right]$$
le système d'équation à alors une infinité de solution. Cela est du aux fait qu'il à deux pivot mais 3 variable.