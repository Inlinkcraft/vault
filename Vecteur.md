---
name: Vecteur
type: Matière
---
#MAT-2930

Un [[Vecteur|vecteur]] est une façons de représenter un couple de valeur numérique qui peut représenter une point dans un plan cartésiens. Celui-ci à un sens, direction et longueur.

> [!Info]
> Deux vecteur sont équivalent si et seulement si:
> - Longueur
> - Direction
> - Sens
> 
> sont égale entre les deux vecteur

### Représentation mathématique
---
Les vecteur en mathématique sont représenter par des lettre minuscule avec une flèche aux dessus.
$$\vec{a} = \vec{OA} = \left[\array{a_{1} \\ a_{2} \\ \vdots}\right]$$

> [!Info]
> La représentation majuscule $\vec{OA}$ signifie un vecteur allant du point $O$ aux point $A$
> $$\vec{AB} = \left[\array{b_{1} \\ b_{2}}\right] - \left[\array{a_{1} \\ a_{2}}\right]$$

### Vecteur nul
---
Le vecteur nul est le vecteur où tous ces composante sont égale à 0.
$$\vec{0} = \left[\array{0 \\ 0 \\ \vdots}\right]$$

### Opération mathématique 
---
#### Addition de vecteur
$$\vec{a} + \vec{b} = \left[\array{a_{1} \\ a_{2}  \\ \vdots }\right] + \left[\array{b_{1} \\ b_{2} \\ \vdots}\right] = \left[\array{a_{1} + b_{1} \\ a_{2} + b_{2}  \\ \vdots }\right]$$

#### Soustraction de vecteur
$$\vec{a} - \vec{b} = \vec{a} + (-\vec{b}) = \left[\array{a_{1} \\ a_{2}  \\ \vdots }\right] - \left[\array{b_{1} \\ b_{2} \\ \vdots}\right] = \left[\array{a_{1} \\ a_{2}  \\ \vdots }\right] + \left[\array{-b_{1} \\ -b_{2} \\ \vdots}\right] = \left[\array{a_{1} - b_{1} \\ a_{2} - b_{2}  \\ \vdots }\right]$$

#### Multiplication par un scalaire
$$n\vec{a} = n\left[\array{a_{1} \\ a_{2}  \\ \vdots }\right] = \left[\array{na_{1} \\ na_{2}  \\ \vdots }\right]$$

### Combinaison Linéaire
---
La combinaison linéaire est une combinaison de $n$ vecteur et $n$ scalaire afin de décrire une espace. Les constante permette de naviguer cet espace.
$$\vec{y} = c_1\vec{v_{1}} + c_2\vec{v_{2}}$$

> [!info] Indépendance linéaire
> L'indépendance linéaire est lorsque qu'un vecteur ne peut pas être décrit à l'aide d'une combinaison linéaire de d'autre vecteur. En d'autre mots le [[Vecteur#Produit scalaire (dot product)|produit scalaire]] est égale à $0$

### Produit scalaire (dot product)
---
Le produit scalaire permet de trouver la norme et différente propriété d'un vecteur.
$$\vec{u} \cdot \vec{v} = u_{1}v_{1} + u_{2}u_{2} + \dots + u_{i}v_{i} = a$$

#### Trouver la norme
Trouver la [[Norme|norme]], longueur du vecteur.
$$||\vec{u}|| = \sqrt{\vec{u} \cdot \vec{u}}$$

> [!Info] Inégalité du triangle
> Le plus long que l'addition de deux vecteur peut être ces quand il on le même sens
> $$||\vec{u} + \vec{v}|| \le ||\vec{u}|| + ||\vec{v}||$$


### Propriété des vecteur
---
#### Vecteur unitaire
Vecteur avec une longueur égale à 1:
$$\vec{u_\vec{v}} = \frac{\vec{v}}{||\vec{v}||}$$

#### Distance entre deux vecteur
La distance entre les extrémité des vecteur:
$$d(\vec{u}, \vec{v}) = ||\vec{u} - \vec{v}||$$

#### Angle entre deux vecteur
L'angle entre les deux vecteur:
$$\cos\theta = \frac{\vec{u} \cdot \vec{v}}{||\vec{u}|| \ ||\vec{v}||}$$

#### Vecteur orthogonaux
Vecteur avec un angle de $90\degree$ entre les deux:
$$0 = \vec{u} \cdot \vec{v}$$

#### Projection d'un vecteur
Le vecteur est projeter sur l'autre:
$$\text{proj}_\vec{u}\vec{v} = \left(\frac{\vec{u} \cdot \vec{v}}{\vec{u} \cdot \vec{u}} \right) \vec{u}$$
