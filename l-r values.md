---
name: l-r values
type: Matière
---
#GLO-2100

[[l-r values]] est un concept un peu abstrait qui consiste a séparé chaque commande d'assosiation en deux "zone". Cela permet d'optimiser le comportement de nos application et ce processus est aider par les [[Class#Constructeur déplacement|constructeurs déplacements]]

```cpp
int var = 2 + 3
```

### signification
---
#### l-value
Le l-value est ce qui ce retrouve a gauche du symbole =. Dans ce cas ici `int var` est le l-value.
```c++
int& x; // est une référance à un r-value
```

> [!tip] Euréka
> Dans ce cas le résultat sera copier à l'adresse de x

#### r-value
Le r-value est ce qui ce retrouve a droite du symbole =, Dans ce cas ici `2 + 3` est le r-value. Le r-value n'a pas d'adresse fixe, ces une adresse temporaire.
```cpp
int&& x; // est une référance à
```

> [!tip] Euréka
> Dans ce cas la référence pointeras directement le resultat.

### Outils de la librairie standard
---
Pour effectuer des opération de la sorte avec des [[Smart pointer|smarts pointers]] il suffit d'utilisée:
```cpp
ptrB = std::move(ptrA);
```

Cet outil permet de déplacer les donné de `ptrA` vers `ptrB`. On peut dire que l'objet représenter par le `ptrB` vole les information à l'objet au `ptrA`. 