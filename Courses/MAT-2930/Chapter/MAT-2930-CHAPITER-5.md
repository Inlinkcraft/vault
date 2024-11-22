---
name: Orthogonalité
type: Chapter
course: MAT-2930
---
#school/MAT-2930 
***
# Orthogonalité

---
## Projection

### Definition
Quel est le point $p$ dans $\vec{u}$ le plus près de $\vec{v}$ ([[Chapitre-5b.pdf#page=2&selection=38,0,44,0&color=yellow|Chapitre-5b, p.2]])
    Le vecteur d'erreur $\vec{e}$ est orthogonal aux vecteur $\vec{u}$

$$\text{proj}_{u}(v) = \left( \frac{u*v}{u * u} \right)u$$
### Matrice de projection

> [!Attention]
> Ça n’est pas la même matrice projection qu’en infographie. On parle ici de projection dans un sous-espace, tandis qu’en infographie il s’agissait plutôt d’une projection de perspective
([[Chapitre-5b.pdf#page=4&selection=6,0,16,64&color=yellow|Chapitre-5b, p.4]])

$$\text{proj}_{u}(v) = \left( \frac{u*v}{u * u} \right)u \to \left( \frac{uu^{T}}{u^{T}u} \right)v \to P \vec{v}$$
$P$ est la matrice de projection
$$P = \left( \frac{uu^{T}}{u^{T}u} \right)$$
Dans $\mathbb{R}^2$ :
$$\begin{bmatrix}
u_{1} \\
u_{2}
\end{bmatrix}
\begin{bmatrix}
u_{1} & u_{2}
\end{bmatrix} = 
\begin{bmatrix}
u_{1}u_{1} & u_{2}u_{1} \\
u_{1}u_{2} & u_{1}u_{2}
\end{bmatrix} =
\begin{bmatrix}
u_{1}\begin{bmatrix}
u_{1} \\
u_{2}
\end{bmatrix} &
u_{2} \begin{bmatrix}
u_{1} \\
u_{2}
\end{bmatrix}
\end{bmatrix}
$$
#### Exemple
[[Chapitre-5b.pdf#page=6&selection=0,8,14,7&color=note|Chapitre-5b, p.6]]

$$P = \frac{1}{5} \begin{bmatrix}
2 \\
1
\end{bmatrix}
\begin{bmatrix}
2 & 1
\end{bmatrix} = \frac{1}{5} \begin{bmatrix}
4 & 2 \\
2 & 1
\end{bmatrix} \Rightarrow
\vec{p} = P\vec{v} = \frac{1}{5} \begin{bmatrix}
4 & 2 \\
2 & 1
\end{bmatrix}\begin{bmatrix}
-5 \\
2
\end{bmatrix} = 
\begin{bmatrix}
-\frac{8}{5} \\
-\frac{4}{5}
\end{bmatrix}
$$

### Propriété

$$P^{T} = P$$
$$P^{k} = P$$

si $\vec{u}$ est unitaire ?
$$P = \frac{uu^{T}}{u^{T}u} = 1$$

### Dans $\mathbb{R}^{3} \to \mathbb{R}^2$ :
Sous-espace $\mathscr{U}$ à 2 dimensions ayant comme base orthonormée $\{u_{1}, u_{2}\}$([[Chapitre-5b.pdf#page=9&selection=28,1,33,16&color=yellow|Chapitre-5b, p.9]])
Quel est le point $p$ dans $\mathscr{U}$ le plus près de $\vec{v}$? ([[Chapitre-5b.pdf#page=9&selection=43,0,49,1&color=yellow|Chapitre-5b, p.9]])

$\to$ Le vecteur projeter aura des valeur en fonction de $u_{1}$ et $u_{2}$

$$\vec{p} = \frac{u_{1}^{T}v}{u_{1}^{T}u_{1}}u_{1} + \frac{u_{2}^{T}v}{u_{2}^{T}u_{2}}u_{2}$$
Projection pour chacun des vecteur du sous-espace

### Théorème de la décomposition orthogonale
([[Chapitre-5b.pdf#page=10&selection=0,0,0,40&color=yellow|Chapitre-5b, p.10]])
Soit $\mathscr{U}$ un sous-espace de $\mathbb{R}^n$. Tout vecteur $v \in \mathbb{R}^n$ peut être écrit sous la forme ([[Chapitre-5b.pdf#page=10&selection=45,0,51,29&color=yellow|Chapitre-5b, p.10]])
$$v = \hat{v} + z$$
$\hat{v}$ : Projection de $\vec{v}$ dans $\mathscr{U}$ 
$z$ : Erreur

$$\hat{v} = \frac{u_{1}^{T}v}{u_{1}^{T}u_{1}}u_{1} + \frac{u_{2}^{T}v}{u_{2}^{T}u_{2}}u_{2} + \dots + \frac{u_{p}^{T}v}{u_{p}^{T}u_{p}}u_{p}$$
##### On peut également écrire cette projection sous la forme Matricielle
([[Chapitre-5b.pdf#page=11&selection=72,0,72,56&color=yellow|Chapitre-5b, p.11]])

$$\hat{v} = \frac{u_{1}u_{1}^{T}}{u_{1}^{T}u_{1}}v + \frac{u_{2}u_{2}^{T}}{u_{2}^{T}u_{2}}v + \dots + \frac{u_{p}u_{p}^{T}}{u_{p}^{T}u_{p}}v$$
$$\hat{v} = \left(\frac{u_{1}u_{1}^{T}}{u_{1}^{T}u_{1}} + \frac{u_{2}u_{2}^{T}}{u_{2}^{T}u_{2}} + \dots + \frac{u_{p}u_{p}^{T}}{u_{p}^{T}u_{p}}\right)v$$

#### Exemple ([[Chapitre-5b.pdf#page=12&selection=0,7,0,7&color=note|Chapitre-5b, p.12]])
$$\begin{bmatrix}
-1 & 1 & 1 &-1
\end{bmatrix} \begin{bmatrix}
2 \\
4 \\
2 \\
4
\end{bmatrix}=
\frac{1}{4}(-2+4+2-1) = \frac{1}{4}(0) = 0$$
$$\begin{bmatrix}
-1 & 1 & -1 &1
\end{bmatrix} \begin{bmatrix}
2 \\
4 \\
2 \\
4
\end{bmatrix}=
\frac{1}{4}(-2+4-2+1) = 1$$
$$\hat{v} = 1\vec{u_{2}}$$
$$z = \begin{bmatrix}
3 \\
3 \\
3 \\
3
\end{bmatrix}$$

#### Exemple ([[Chapitre-5b.pdf#page=14&selection=0,7,0,7&color=note|Chapitre-5b, p.14]])
$$\hat{v_{2}} = \begin{bmatrix}
-1 \\
1 \\
1 \\
-1
\end{bmatrix} + 2 \begin{bmatrix}
-1 \\
1 \\
-1 \\
1
\end{bmatrix} = \begin{bmatrix}
-3 \\
3 \\
-1 \\
1 \\
\end{bmatrix}$$
$$z = \begin{bmatrix}
0 \\
0 \\
0 \\
0
\end{bmatrix}$$
#### Exemple ([[Chapitre-5b.pdf#page=14&selection=0,0,0,7&color=note|Chapitre-5b, p.14]])
$$\hat{v_{3}} = \begin{bmatrix}
0 \\
0 \\
0 \\
0
\end{bmatrix}$$
$$z = \vec{v_{3}}-\hat{v_{3}} = \vec{v_{3}}$$

---

## Matrices orthogonales

### Base orthonormée ([[Chapitre-5c.pdf#page=2&selection=0,16,0,16&color=yellow|Chapitre-5c, p.2]])
Une base formée de vecteur $q_{1},q_{2}, \dots$ tel que:
$$q_{i}^{T}q_{j} = \begin{cases}
i \ne j : 0 \\
i = j : 1
\end{cases}$$

### Matrice orthogonale (ou orthonormale) ([[Chapitre-5c.pdf#page=3&selection=0,0,0,37&color=yellow|Chapitre-5c, p.3]])
Colonnes = vecteurs orthonormaux

$$Q^{T}Q = \begin{bmatrix}
q_{1}^{T}q_{1} & \dots \\
\vdots & \ddots
\end{bmatrix} = I$$
---
## Méthode de Gram-Schmidt

La méthode de Gram-Schmidt permet de trouver une base orthogonale (et même orthonormale) du même sous-espace
([[Chapitre-5d.pdf#page=2&selection=16,0,18,54&color=yellow|Chapitre-5d, p.2]])

### Cas à deux vecteurs
On à un sous-espace $x_{1}, x_{2}$
On pose $v_{1} = x_{1}$
On veut $v_{2}$ soit perpendiculaire à $v_{1}$ tous en étant dans le même sous-espace donc
$v_{2} = x_{2} - \frac{x_{2}^Tv_{1}}{v_{1}^Tv_{1}}v_{1}$ soit le vecteur erreur…
Finalement on normalise

### Cas à un 3e vecteurs
On à un sous-espace $x_{1}, x_{2}, x_{3}$
$v_{1} = x_{1}$
$v_{2} = x_{2}-\frac{x_{2}^{T}v_{1}}{v_{1}^Tv_{1}}v_{1}$
$v_{3} = x_{3}-\frac{x_{3}^{T}v_{1}}{v_{1}^Tv_{1}}v_{1}-\frac{x_{3}^{T}v_{2}}{v_{2}^Tv_{2}}v_{2}$

### Cas à un 4e vecteurs
On à un sous-espace $x_{1}, x_{2}, x_{3}$
$v_{1} = x_{1}$
$v_{2} = x_{2}-\frac{x_{2}^{T}v_{1}}{v_{1}^Tv_{1}}v_{1}$
$v_{3} = x_{3}-\frac{x_{3}^{T}v_{1}}{v_{1}^Tv_{1}}v_{1}-\frac{x_{3}^{T}v_{2}}{v_{2}^Tv_{2}}v_{2}$
$v_{4} = x_{4}-\frac{x_{4}^{T}v_{1}}{v_{1}^Tv_{1}}v_{1}-\frac{x_{4}^{T}v_{2}}{v_{2}^Tv_{2}}v_{2}-\frac{x_{4}^{T}v_{3}}{v_{3}^Tv_{3}}v_{3}$

### Exemple ([[Chapitre-5d.pdf#page=7&selection=0,7,0,7&color=note|Chapitre-5d, p.7]])

$v_{1} = \begin{bmatrix} 1  \\  1  \\  1\end{bmatrix}$
$v_{2} = \begin{bmatrix}1  \\ 0 \\ 2\end{bmatrix} - \frac{1}{3}\begin{bmatrix}1 & 0 & 2\end{bmatrix} \begin{bmatrix}1  \\  1  \\ 1 \end{bmatrix} = \begin{bmatrix}0  \\ -1 \\ 1\end{bmatrix}$
$q_{1}=\begin{bmatrix} \frac{1}{\sqrt{ 3 } } \\ \frac{1}{\sqrt{ 3 } } \\ \frac{1}{\sqrt{ 3 } } \end{bmatrix}$
$q_{2}=\begin{bmatrix} 0 \\ \frac{1}{\sqrt{ 2 } } \\ \frac{1}{\sqrt{ 2 } } \end{bmatrix}$

Quelle est la relation entre l’espace des colonnes de et celui de ? ([[Chapitre-5d.pdf#page=8&selection=4,0,8,1&color=yellow|Chapitre-5d, p.8]])
C'est le même !!

### Une nouvelle sorte de factorisation ?
$A \to Q$
Une autre matrices va apparaitre qui se nommera $R$ où
$$A = QR$$