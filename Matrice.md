---
name: Matrice
type: Matière
---
#MAT-2930

Une matrice est une regroupement de [[Vecteur|vecteur]] dans le but de produire une grille a plusieurs dimension.

### Représentation matriciel d'une équation linéaire
---
Pour représenter une équation linéaire de la forme $a_{1}x_{1} + a_{2}x_{2} +  \dots+ a_{n}x_{n} = b$ à la forme matriciel on utilise:
$$A\vec{x} = \vec{b}$$

- $A$ est la matrice des coefficient
    - 1 ligne de la matrice : 1 équation
    - 1 colonne : 1 variable ($x_n$)
- $\vec{x}$ est le vecteur des inconnue
- $\vec{b}$ est le vecteur des connue

>[!Note]- Version developer
>$$
>\left[ 
>\array
>{
>a_{11} & a_{12} & \dots & a_{1n} \\
>a_{21} & a_{22} & \dots & a_{2n} \\
>\vdots & \vdots & \ddots & \vdots \\
>a_{m1} & a_{m2} & \dots & a_{mn} \\
>}
>\right]
>\left[ 
>\array
>{
>x_{1} \\
>x_{2} \\
>\vdots \\
>x_{n} \\
>}
>\right]
>=
>\left[ 
>\array
>{
>b_{1} \\
>b_{2} \\
>\vdots \\
>b_{m} \\
>}
>\right]
>$$

>[!info]
> Une équation linéaire peut avoir $\infty, 1 \ \text{ou} \ 0$ solution possible

### Matrice augmenté
---
Une matrice augmenté est une représentation simplifier d'une [[Vecteur#Combinaison Linéaire|combinaison linéaire]].

$$\left[ 
\begin{array}{cccc|c}
a_{11} & a_{12} & \dots & a_{1n} & b_1 \\
a_{21} & a_{22} & \dots & a_{2n} & b_2\\
\vdots & \vdots & \ddots & \vdots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn} & b_m\\ 
\end{array}
\right]$$

> [!Info]
> $\vec{x}$ : est sous-entendue dans la matrice

> [!Info]
> Lorsqu'on parle d'un rang d'une matrice nous faisons le compte du nombre de ligne qui n'est pas égale à zero

### Type de matrice
---
#### Matrice carré
Une matrice qui a le même nombre de colonne et de ligne
$$\left[ 
\begin{array}{cccc}
a_{11} & a_{12} & a_{13} & a_{14} \\
a_{21} & a_{22} & a_{23} & a_{24} \\
a_{31} & a_{32} & a_{33} & a_{34} \\ 
a_{41} & a_{42} & a_{43} & a_{44} \\ 
\end{array}
\right]$$

#### Matrice diagonal
généralement carré aussi
$$\left[ 
\begin{array}{cccc}
a_{11} & 0 & 0 & 0 \\
0 & a_{22} & 0 & 0 \\
0 & 0 & a_{33} & 0 \\ 
0 & 0 & 0 & a_{44} \\ 
\end{array}
\right]$$

#### Matrice scalaire
Contient seulement un scalaire
$$\left[ 
\begin{array}{cccc}
k & 0 & 0 & 0 \\
0 & k & 0 & 0 \\
0 & 0 & k & 0 \\ 
0 & 0 & 0 & k \\ 
\end{array}
\right]$$

#### Matrice identité
Contient seulement un
$$\left[ 
\begin{array}{cccc}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\ 
0 & 0 & 0 & 1 \\ 
\end{array}
\right]$$

## Opération matriciel
#### Adition
$$\left[ 
\begin{array}{cc}
a_{11} & a_{12} \\
a_{21} & a_{22} \\
\end{array}
\right] + \left[ 
\begin{array}{cc}
b_{11} & b_{12} \\
b_{21} & b_{22} \\
\end{array}
\right] = \left[\begin{array}{cc}
a_{11} + b_{11} & a_{12} + b_{12}\\
a_{21} + b_{21} & a_{22} + b_{22}\\
\end{array}\right]$$

#### Multiplication par un scalaire
$$k\left[ 
\begin{array}{cc}
a_{11} & a_{12} \\
a_{21} & a_{22} \\
\end{array}
\right] = \left[ 
\begin{array}{cc}
ka_{11} & ka_{12} \\
ka_{21} & ka_{22} \\
\end{array}
\right] $$

#### Transposition
$$\left(\left[ 
\begin{array}{cc}
a_{11} & a_{12} \\
a_{21} & a_{22} \\
\end{array}
\right]\right)^{T} = \left[ 
\begin{array}{cc}
a_{11} & a_{21} \\
a_{12} & a_{22} \\
\end{array}
\right] $$
#### Multiplication matriciel
$$\left[ 
\begin{array}{cc}
a_{11} & a_{12} \\
a_{21} & a_{22} \\
\end{array}
\right] \times \left[ 
\begin{array}{cc}
b_{11} & b_{12} \\
b_{21} & b_{22} \\
\end{array}
\right] =  \left[ 
\begin{array}{cc}
a_{11}b_{11} + a_{12}b_{21} & a_{11}b_{12} + a_{12}b_{22} \\
a_{21}b_{11} + a_{22}b_{21} & a_{21}b_{12} + a_{22}b_{22} \\
\end{array}
\right]$$
##### 4 Interprétation de la multiplication matriciel
###### ligne A X colonne B
Soit la multiplication des ligne de a par les colonne de b
$$c_{ij} = \sum_{k=1}^{n} a_{ik}b_{kj}$$
###### Par colonne B
Soit une [[Vecteur#Combinaison Linéaire|combinaison linéaire]] des colonne de b
$$\text{col}_{k}(C) = A\text{col}_{k}(B)$$
###### Par ligne A
Soit une [[Vecteur#Combinaison Linéaire|combinaison linéaire]] des ligne de A
$$\text{ligne}_{l}(C) = \text{ligne}_{l}(A)B$$
###### colonne X ligne
Soit la multiplication des ligne de a par les colonne de b
$$c_{ij} = \sum_{k=1}^{n} \text{col}_{k}(A)\text{ligne}_{k}(B)$$

#### Puissance de matrice carré
La puissance d'une matrice carré va comme suit:
$$A^{x} = \underbrace{A \times A \times \dots \times A}_{x \text{ fois}}$$

### Conditionnement
---
Le [[Matrice#Conditionnement|conditionnement]] d'une matrice mesure la dépendance de ces paramètre sur sa solution. 

> Conditionnement faible (1) est un problème bien conditionné (stable)
> Conditionnement élevé (>>1) est un problème mal conditionné

Pour remédier aux problème de précision nous s'assurons que le pivot ayant la plus grande valeur absolu soit le pivot supérieur.