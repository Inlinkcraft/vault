---
name: MatLab
type: wiki
---
#GEL-1000 #MAT-2930 

MatLab fonctionne par indexage par base 1

### Affichage de valeur
---
Le `;` sert a retiré l'affichage du résultat d'une ligne
Pour afficher une variable il suffit de l'écrire: `x` afficheras la valeur de `x` tandis que `x;` n'afficheras pas la valeur de `x`.

#### Commentaire
Pour écrire une commentaire il suffit d'ajouter `%` aux début de la ligne
```MATLAB
% Ceci est un commentaire ;P
```

### Construction d'un vecteur
---
Pour construire une [[Vecteur|vecteur]] il suffit d'écrire:
```MATLAB
x = a:s:b
```
- `a` est la borne de départ
- `s` est l'écart entre chacune des valeur
- `b` est la borne final

### Construire une matrice
---
Pour construire une [[Matrice|matrice]] il suffit d'écrire:
```MATLAB
M = [a, b, c; e, f, g; h, i, j]
```

#### Dimension d'une matrice
Pour avoir la dimension d'une [[Matrice|matrice]] : `size(M)`

### Afficher un graphique
---
Pour afficher un graphique on utilise:
```MATLAB
plot(x, y)
plot(x, y, caracthéristique...)
```
- `x` et `y` sont des vecteur de même taille décrivant les points
- `caracthéristique`: Les caractéristique sont une liste d'affectation à la courbe
    - `g` : Ligne grasse
    - `*` : Juste les points
    - `LineWidth = 4`: Largeur de la ligne

### Boucle
---
#### For loop
Pour faire une boucle for:
```
for i = a:b
    % Code
end
```
- `i = a:b`; `i` parcourra les valeur de `a` à `b`