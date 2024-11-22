---
name: Méthode des maille
type: Matière
---
#GEL-1000 

La méthode des maille est une procédure qui permet de résoudre un [[Circuit électrique|circuit]] avec $m$ équations en utilisant les [[Courant circulatoire]]. En d'autre mots le but de la méthode des maille est d'exprimer les [[Courant électrique|courant]] de tous les branche du [[Circuit électrique|circuit]] en fonction des [[Courant circulatoire|courant circulatoire]].

> [!Info]
> Utile si il y a trop de [[Nœud|noeud]]

### Procédure
---
#### Procédure matriciel
---
La plus rapide des deux procédure mes demande une plus grande compréhension.
$$
\begin{array}{c}
M_{1} \\
M_{2} \\
M_{3} \\
\vdots\\
M_{m}
\end{array}
\quad
\left[\begin{array}{ccccc}
R_{11} & -R_{12} & -R_{13} & \dots & -R_{1m} \\
-R_{21} & R_{22} & -R_{23} & \dots & -R_{2m} \\
-R_{31} & -R_{32} & R_{33} & \dots & -R_{3m} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
R_{m1} & -R_{m2} & -R_{m3} & \dots & -R_{mm} \\
\end{array}\right]
\cdot
\left[\begin{array}{c}
I_{1} \\
I_{2} \\
I_{3} \\
\vdots\\
I_{m}
\end{array}\right]
=
\left[\begin{array}{c}
V_{1} \\
V_{2} \\
V_{3} \\
\vdots\\
V_{m}
\end{array}\right]
$$

Soit:
- $\vec{I}$ : [[Vecteur|Vecteur]] des [[Courant circulatoire|courant circulatoire]]
- $\vec{V}$ : [[Vecteur|Vecteur]] des [[Tension électrique|tension]] dans les  [[Maille|maille]] dus aux [[Source électrique|source]]
    - $V_i$: La somme des [[Tension électrique|tension]] dans la [[Maille|maille]] $i$ dus aux [[Source électrique|source]]
- $R$ : matrice des [[Résistance électrique|Résistance]]
    - La matrice est symétrique
    - $R_{ii}$ : Somme des [[Résistance électrique|Résistance]] dans la [[Maille|maille]] $i$
    - $R_{ij}$ : Somme des [[Résistance électrique|Résistance]] commune aux [[Maille|maille]] $i$ et $j$

#### Procédure logique
---
Cette procédure permet de comprendre la procédure matriciel

##### Étape 1
Construire le [[Circuit de base|circuit de base]].

##### Étape 2
Définir les [[Courant circulatoire|courant circulatoire]].

##### Étape 3
Exprimer les [[Courant électrique|courant]] dans les branches en fonction des [[Courant circulatoire|courant circulatoire]].

##### Étape 4
Écrire les [[Lois de Kirchhoff#Lois des tension|équations de Kirchhoff des tension]] pour les m maille.

##### Étape 5
Écrire les équations caractéristiques v-i des [[Élément électrique|éléments]].

##### Étape 6
Insérer les relations v-i dans les [[Lois de Kirchhoff#Lois des tension|équations de tension]] **(de l’étape 4)**

##### Étape 7
Insérer les relations de **l’étape 3** dans les équations obtenues à **l’étape 6**