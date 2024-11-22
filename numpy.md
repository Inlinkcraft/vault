---
name: numpy
type: Wiki
---
#MAT-2930
### Manipulation de vecteur
---
- `np.array(arr)`: Crée un [[Vecteur|vecteur]]
- `np.linalg.norm(arr)`: Permet de normalisé le [[Vecteur|vecteur]]
- `np.dot(arr1, arr2)`: Effectue le produit scalaire du [[Vecteur|vecteur]]
- `np.linspace(min, max, step)`: Crée un [[Vecteur|vecteur]] incluant tous les valeurs entre `min` et `max` à un intervalle équivalent à `(max-min)/step`

### Manipulation de matrice
---
- `np.array(arr)`: Créé une [[Matrice|matrice]]
- `A[r, c]`: permet d'optenir la valeur à la coordonnée `(r, c)` de la [[Matrice|matrice]]. `r` ou `c` peuvent être:
    - Un [[Vecteur|vecteur]] d'indice
    - `from:to`: prend tous entre `from`(inclusif) à `to`(exclusif)
- `np.column_stack((arr, c))`: Permet d'ajouter une colonne à la fin de la [[Matrice|matrice]]
- `np.concatenate((arr, c), axis=a)`:Permet d'ajouter une ligne ou colonne selon l'axis
    - `a = 0`: ligne, `a = 1`: colonne.
- `array.reshape(r, c)`: Permet de redimensionner une [[Matrice|matrice]].
    - `-1`: Dans les paramètre aura pour effet de donné carte blanche à la dimention
- `np.linalg.solve(coff_arr, b)`: Résout le système d'équation
- `np.copy(arr)`: Créé une copie de la [[Matrice|matrice]].
    - `.astype(type)`: Permet de modifier le type de la [[Matrice|matrice]].