---
name: Méthode itérative
type: Matière
---
#MAT-2930 

La méthode itérative de résolution de [[Matrice|matrice]] est une méthode qui cherche a simplifier la recherche d'une solution.

### Méthode de Jacobi
---
Méthode purement itérative
##### Étape 1
Isolé chacune des variable de $\vec{x}$
##### Étape 2
Posé $\vec{x}$ tel que $\vec{x} = \vec{0}$
##### Étape 3
Calculer le résultat de chacun des $x_{i}$
##### Étape 4
Lorsque tous les $x_i$ sont calculer recommencer a partir de l'**étape 3**


### Méthode de Gauss-Seidel
---
Méthode plus rapide
##### Étape 1
Isolé chacune des variable de $\vec{x}$
##### Étape 2
Posé $\vec{x}$ tel que $\vec{x} = \vec{0}$
##### Étape 3
Calculer le résultat de $x_{i}$
##### Étape 4
Metter a jour la nouvelle variable et répété l'**étape 3** pour la prochaine valeur

> [!Tip] Matrice à diagonal strictement dominante
> Si la matrice à une diagonals strictement dominante il aura alors une solution unique aux méthode itérative
> $$|a_{11}| > |a_{12}|+ |a_{13}| + \dots + a_{1n}$$
> $$|a_{22}| > |a_{21}|+ |a_{23}| + \dots + a_{2n}$$


