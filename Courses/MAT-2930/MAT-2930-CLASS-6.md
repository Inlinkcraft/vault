---
name: Cours-6
type: Class
course: MAT-2930
date: 2024-09-23T11:30
Complete: true
---
#school/MAT-2930
***

# Système homogène
Un [[Système homogène|système homogène]] est sous forme de [[Matrice|matrice]] ou la réponse a l'équation est le [[Vecteur|vecteur]] nul. Alors une [[Matrice|matrice]] est [[Indépendance linéaire|dépendante linéaire]] si il y a plus que seulement la solution [[Système homogène#Solution trivial|trivial]] aux [[Système homogène|système homogène]]

# Méthode itérative
La [[Méthode itérative|méthode itérative]] de résolution de [[Matrice|matrice]] est une méthode qui cherche a simplifier la recherche d'une solution.

$$\left[ 
\begin{array}{cccc|cccc}
a_{11} & a_{12} & a_{13} & a_{14} & 1 & 0 & 0 & 0 \\
a_{21} & a_{22} & a_{23} & a_{24} & 0 & 1 & 0 & 0 \\
a_{31} & a_{32} & a_{33} & a_{34} & 0 & 0 & 1 & 0 \\
a_{41} & a_{42} & a_{43} & a_{44} & 0 & 0 & 0 & 1 \\ 
\end{array}
\right]$$

Ensuite faire la résolution par [[Algorithme de Gauss-Jordan|algorithme de Gauss-Jordan]]