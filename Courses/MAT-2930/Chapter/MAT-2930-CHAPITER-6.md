---
name: Distance et approcimation
type: Chapter
course: MAT-2930
---
#school/MAT-2930 

# Distance et approximation

Projection revisitées
---
### Projection dans un sous-espace à 1 dim
---
Nou voulons approximer
$$\hat{v} = $$

> [!question] Pourquoi approximer ?
> Car dans plusieurs scenario l'équation $Ax=b$ ne possède aucune solution !
> > [!question] Quand est ce que il n'a pas aucune solution
> > Si on à plus d'équation que d'inconnue
> > soit: $m > n$
> > Dans cette situation la plupart du temps le vecteur $b$ n'est pas dans l'espace des colonnes de $A$
> 
> > [!success] Solution
> > Nous allons résoudre l'équation suivante:
> > $$A \hat{x} = \hat{b}$$
> > Nous allons projeter $b$ dans l'espace des colonnes de $A$. Ce qui nous donnera une approximation à $b$ soit $\hat{b}$

### Projection dans l'espace des colonnes de $A$
---
$$Ax= b \longrightarrow A \hat{x} = \hat{b}$$
Quel est le point $\hat{b}$ le plus proche de $b$ qui se trouve dans l'espace des colonnes de A
> [!attention] Attention
> Les colonnes de $A$ ne sont pas forcément orthogonale
([[Chapitre-6a.pdf#page=4&selection=59,2,61,33&color=red|Chapitre-6a, p.4]])

Sachant que : $\vec{\epsilon} = b - A \hat{x}$ est perpendiculaire au plan, projeter sur un vecteur à la fois
Je souhaite que $\epsilon$ soit perpendiculaire avec $\vec{a_{1}}$ et $\vec{a_{2}}$
	$\vec{a_{1}}^{T}\vec{\epsilon}=0$
	$\vec{a_{1}}^{T}(b-A \hat{x})=0$
	$\vec{a_{2}}^{T}\vec{\epsilon}=0$
	$\vec{a_{2}}^{T}(b-A \hat{x})=0$
	$$\begin{bmatrix}\vec{a_{1}} \\ \vec{a_{2}}\end{bmatrix}(b-A \hat{x}) = \vec{0}$$
	$$A^{T}(\vec{b}-A \hat{x}) = 0$$
	$$A^{T}\vec{\epsilon} = 0$$
([[Chapitre-6a.pdf#page=5&selection=18,0,22,42&color=yellow|Chapitre-6a, p.5]])

##### Dans quel sous-espace est situé $(b-A \hat{x})$ ?
Dans l'espace-null de $A^T$

### Déterminer $\hat{x}$
---
$$A^T(b-A \hat{x}) = 0$$
> [!info] Rappel
> $\hat{x}$ est l'approximation de $\vec{x}$ dans $A \vec{x} = \vec{b}$

$$A^T b - A^TA \hat{x} = 0$$
$$A^TA \hat{x} = A^T b$$
Si $A^TA$ est inversible, alors $$\hat{x} = (A^TA)^{-1}A^Tb$$
Alors $(A^TA)^{-1}A^T$ est la pseudo inverse

> [!info] Lien avec orthogonalité
> $$\hat{x} = (A^TA)^{-1}A^Tb$$
> Projection de b:
> $$\hat{b} = A \hat{x} = A(A^TA)^{-1}A^Tb$$
> Ces le cas général de la projection d'un vecteur $\vec{b}$ dans le sous-espace engendré par les colonnes de $A$ lorsqu'elle ne sont pas orthogonales.
> > [!question] Qu'arrive-t-il si les colonne de $A$ sont orthonormal
> > $$\hat{b} = A(A^TA)^{-1}A^Tb$$
> > Donc sachant notre initialité $(A^TA) = I$
> > $$\hat{b}=AA^Tb$$

### Erreur commise
---
L'erreur commise est
$$\epsilon = ||b - \hat{b}||$$
> [!tip] Erreur quadratique
> L’erreur quadratique moyenne est définie par 
> $$\epsilon^{2} = ||b - \hat{b}||^{2}$$
> ([[Chapitre-6a.pdf#page=9&selection=22,1,50,7&color=yellow|Chapitre-6a, p.9]])

>[!example] Exemple
> $$A=\begin{bmatrix}
 1 & 1 & 0 & 0\\
 1 & 1 & 0 & 0\\
 1 & 0 & 1 & 0\\
 1 & 0 & 1 & 0\\
 1 & 0 & 0 & 1\\
 1 & 0 & 0 & 1
\end{bmatrix}$$
> $$b=\begin{bmatrix}
 -3\\
 -1\\
 0\\
 2\\
 5\\
 1
\end{bmatrix}$$
> 0 solution !
> Qu'elle est la meilleur approximation
> > "Meilleur" Au sens moindre carrés, solution qui minimise l'erreu quadratique moyenne
>  $$A^T=\begin{bmatrix}
 1 & 1 & 1 & 1 & 1 & 1\\
 1 & 1 & 0 & 0 & 0 & 0\\
 0 & 0 & 1 & 1 & 0 & 0\\
 0 & 0 & 0 & 0 & 1 & 1
\end{bmatrix}$$
> $$=\begin{bmatrix}
 6 & 2 & 2 & 2 \\
 2 & 2 & 0 & 0 \\
 2 & 0 & 2 & 0 \\
 2 & 0 & 0 & 2 
\end{bmatrix}$$
> ...
>  $$=\left[\begin{array}{cccc|c}
 6 & 2 & 2 & 2 & 4\\
 2 & 2 & 0 & 0 & -4\\
 2 & 0 & 2 & 0 & 2\\
 2 & 0 & 0 & 2 & 6 
\end{array}\right]$$
> ....

