---
name: Transformation linéaire
type: Matière
---
#MAT-2930 

Les transformation linéaire sont des transformation applicable à des [[Matrice|matrice]] afin d'optenir certain comportement. Ces transformation mettre en jeu des [[Coordonné homogène|coordonné homogène]] qui permettre plus de contrôle pour certaine transformation (ex: [[Transformation linéaire#Translation|translation]])

$$T:\mathbb{R}^{n} \to \mathbb{R}^m$$
$$T(x + y) = T(x) + T(y)$$
$$T(cx) = cT(x)$$

### Transformation courante
---
Voici quelque transformation utiliser fréquemment
#### Facteur échèle
Permet de changer l'échelle d'un objet
###### normal
$$\left[\begin{array}{cc}
S_{x} & 0 \\
0 & S_{y} \\
\end{array}\right]$$

###### [[Coordonné homogène|homogène]]
$$\left[\begin{array}{ccc}
S_{x} & 0 & 0 \\
0 & S_{y} & 0 \\
0 & 0 & 1 \\
\end{array}\right]$$

#### Réflexion
Permet de miroir l'objet selon l'axe x ou y
###### normal
$$\left[\begin{array}{cc}
\pm 1 & 0 \\
0 & \pm 1 \\
\end{array}\right]$$

###### [[Coordonné homogène|homogène]]
$$\left[\begin{array}{ccc}
\pm 1 & 0 & 0 \\
0 & \pm 1 & 0 \\
0 & 0 & 1 \\
\end{array}\right]$$

#### Cisaillement
Permet de cisailler l'objet selon l'axe x ou y
###### normal
$$\left[\begin{array}{cc}
0 & k_{x} \\
k_{y} & 0 \\
\end{array}\right]$$

###### [[Coordonné homogène|homogène]]
$$\left[\begin{array}{ccc}
0 & k_{x} & 0 \\
k_{y} & 0 & 0 \\
0 & 0 & 1 \\
\end{array}\right]$$

#### Rotation
Permet de rotation l'objet selon l'axe z
###### normal
$$\left[\begin{array}{cc}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta \\
\end{array}\right]$$

###### [[Coordonné homogène|homogène]]
$$\left[\begin{array}{ccc}
\cos \theta & -\sin \theta & 0 \\
\sin \theta & \cos \theta & 0 \\
0 & 0 & 1 \\
\end{array}\right]$$


##### Translation
Déplacement seulement possible en [[Coordonné homogène|coordonné homogène]]
$$\left[\begin{array}{ccc}
1 & 0 & t_{x} \\
0 & 1 & t_{y} \\
0 & 0 & 1 \\
\end{array}\right]$$

##### Projection perspective (Oxy)
La projection perspective $Oxy$ est une projection simple qui se présente comme suit en [[Coordonné homogène|coordonné homogène]]:
$$\left[\begin{array}{cccc}
1 & 0 & 0 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & -1/d & 1\\
\end{array}\right]$$
Où $d$ est la distance sur l'axe $z$ de la projection.
