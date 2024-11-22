---
name: Méthode des noeud
type: Matière
---
#GEL-1000 

La méthode des nœud est une procédure qui permet de résoudre un [[Circuit électrique|circuit]] avec $(n-1)$ équations en utilisant les [[Tension nodale]]. En d'autre mots le but de la méthode des nœud est d'exprimer la [[Tension électrique|tension]] de tous les [[Élément électrique|élément]] du [[Circuit électrique|circuit]] en fonction de leur [[Tension nodale|tension nodale]]

### Procédure
---
#### Procédure matriciel
---
La plus rapide des deux procédure mes demande une plus grande compréhension.
$$
\begin{array}{c}
N_{1} \\
N_{2} \\
N_{3} \\
\vdots\\
N_{(n-1)}
\end{array}
\quad
\left[\begin{array}{ccccc}
G_{11} & -G_{12} & -G_{13} & \dots & -G_{1(n-1)} \\
-G_{21} & G_{22} & -G_{23} & \dots & -G_{2(n-1)} \\
-G_{31} & -G_{32} & G_{33} & \dots & -G_{3(n-1)} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
G_{(n-1)1} & -G_{(n-1)2} & -G_{(n-1)3} & \dots & -G_{(n-1)(n-1)} \\
\end{array}\right]
\cdot
\left[\begin{array}{c}
V_{1} \\
V_{2} \\
V_{3} \\
\vdots\\
V_{(n-1)}
\end{array}\right]
=
\left[\begin{array}{c}
I_{1} \\
I_{2} \\
I_{3} \\
\vdots\\
I_{(n-1)}
\end{array}\right]
$$

Soit:
- $\vec{V}$ : [[Vecteur|Vecteur]] des [[Tension nodale|tensions nodales]]
- $\vec{I}$ : [[Vecteur|Vecteur]] des [[Courant électrique|courant]] qui arrivent aux [[Nœud|nœud]] dus aux [[Source électrique|source]]
    - $I_i$: La somme des [[Courant électrique|courant]] arrivant au [[Nœud|nœud]] $i$ dus aux [[Source électrique|source]]
- $G$ : matrice des [[Conductance|conductance]]
    - La matrice est symétrique
    - $G_{ii}$ : Somme des [[Conductance|conductance]] touchant directement au [[Nœud|nœud]] $i$
    - $G_{ij}$ : Somme des [[Conductance|conductance]] reliant de manière directe les [[Nœud|nœud]] $i$ et $j$

#### Procédure logique
---
Cette procédure permet de comprendre la procédure matriciel

##### Étape 1
Construire le [[Circuit de base|circuit de base]].

##### Étape 2
Choisir les $(n - 1)$ [[Tension nodale|tension nodale]]

##### Étape 3
Exprimer les [[Tension électrique|tension]] dans les branches en fonction des [[Tension nodale|tension nodale]].

##### Étape 4
Écrire les [[Lois de Kirchhoff#Lois des courant|équations de Kirchhoff des courants]] pour les (n-1) nœuds.

##### Étape 5
Écrire les équations caractéristiques v-i des [[Élément électrique|éléments]].

##### Étape 6
Insérer les relations v-i dans les [[Lois de Kirchhoff#Lois des courant|équations de courants]] **(de l’étape 4)**

##### Étape 7
Insérer les relations de **l’étape 3** dans les équations obtenues à **l’étape 6**