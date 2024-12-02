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

Moindres carrés
---
![[Chapitre-6b.pdf#page=2&rect=642,45,1270,515|Chapitre-6b, p.2]]

##### L'équation normale
$$A^{T}A \hat{x} = A ^{T}b$$
> [!info] 
> Ici $\hat{x}$ est la solution aux moindres carrés car elle minimise l'erreur quadratiques moyenne

> [!example] Example
>  $$p \to \{(1,1), (2, 2), (3, 2)\}$$
>  On cherche la meilleur droite pour représenter ces point
>  $\to$ objectif répartir l'erreur sur tous les point pour minimiser la somme des erreur aux carrée
>  - $p_{1} : 1 = C + D$
>  - $p_{2} : 2 = C + 2D$
>  - $p_{3} : 2 = C + 3D$
>  Avec une matrice
>  $$\begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \end{bmatrix} \begin{bmatrix} C \\ D \end{bmatrix} = \begin{bmatrix}1 \\ 2 \\ 2 \end{bmatrix}$$
>  > [!attention] Aucune solutoion
>  > **Interpretation**: $b$ n'est pas dans les colonne de $A$
>  > Il n'y a pas de droite qui passe par les 3 points
>  
>  Trouvons les $\hat{C}$ et $\hat{D}$ qui minimiserons notre erreur
>  $$A^TA \hat{x} = A^{T}b$$
>  $$\begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \end{bmatrix} \begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \end{bmatrix} = \begin{bmatrix}3 & 6 \\ 6 & 14\end{bmatrix} \qquad \begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \end{bmatrix}\begin{bmatrix}1 \\ 2 \\ 2 \end{bmatrix}= \begin{bmatrix}5 \\ 11\end{bmatrix}$$
>  $$\begin{bmatrix}3 & 6 \\ 6 & 14\end{bmatrix}\begin{bmatrix} \hat{C} \\ \hat{D} \end{bmatrix} = \begin{bmatrix}5 \\ 11\end{bmatrix} \to \begin{bmatrix} 3 & 6 & 5 \\ 6 & 14 & 11 \end{bmatrix}$$
>  ...
>  $$x_{2} = \frac{2}{3}+\frac{1}{2}x_{1}$$
>  Maintenant quelle est notre erreur ?
>  $$\epsilon_{1} = \frac{1}{6} \quad \epsilon_{2} = -\frac{2}{6} \quad \epsilon_{3} = \frac{1}{6}$$
>  Erreur quadratique moyenne ?:
>  $$\left( \frac{1}{6} \right)^{2} + \left( -\frac{2}{6} \right)^{2} + \left( \frac{1}{6} \right)^{2}$$
>
>  [[Chapitre-6b.pdf#page=4&color=yellow|Chapitre-6b, p.4]]

### Inversibilité
---
Matrice pseudo inverse
$$\hat{x} = \underbrace{(A^TA)^{-1}A^{T}}_{\text{pseudo inverse}}b$$
Si les colonnes de $A$ sont linéairement indépendantes, alors $A^TA$ est inversible.
([[Chapitre-6b.pdf#page=8&selection=4,0,8,15&color=yellow|Chapitre-6b, p.8]])

> [!important] Preuve
> $$A^TAx = 0$$
> démontrons que la seule solution possible est $x = 0$
> multiplions par $x^T$
> $$x^TA^TAx = 0$$
> $$(Ax)^TAx = 0$$
> renommons $v = Ax$
> $$v^Tv = 0$$
> $$||v||^2 = 0$$
> $$v = 0$$
> Si les colonne de $A$ sont indépendante la seule solution possible ces $x = 0$

### Factorisation QR
---
Peut-on utiliser la factorisation QR pour résoudre l’équation normale ([[Chapitre-6b.pdf#page=9&selection=20,0,20,69&color=yellow|Chapitre-6b, p.9]])
$$A = QR$$
$$(QR)^TQR \hat{x} = (QR)^T b$$
$$R^TQ^TQR \hat{x} = R^TQ^Tb$$
$$R^TR \hat{x} = R^TQ^Tb$$
$$R \hat{x} = Q^T b$$
$$\hat{x} = R^{-1}Q^Tb$$
### Orthogonalité
---
Si les colonnes de sont orthonormales ([[Chapitre-6b.pdf#page=10&selection=20,0,22,18&color=yellow|Chapitre-6b, p.10]]):
$$A^TA=I$$
alors $\hat{x} = A^Tb$