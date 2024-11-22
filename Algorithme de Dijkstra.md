---
name: Algorithme de Dijkstra
type: Matière
---
#GLO-2100 

L'algorithme de Dijkstra permet de trouver le chemin le plus cours dans un [[Graph|graph]] pondéré qui n'a pas de valeur négative.

### Implementation
---
```pseudocode
POUR TOUT v DANS s FAIRE:
    d(v) = INF;
    p(v) = NIL;
d(s) = 0
T = {} // noeuds solutionné
Q = S  // noeuds à solutionné
RÉPÉTER |S| FOIS
    u* = u DE Q AVEC MIN(d(u)) 
    Q.RETIRER(u*)
    T.AJOUTER(u*)
    POUR TOUT u DANS Q VOISIN DE u* FAIRE
        temp = d(u*) + w(u*, u)
        SI temp < d(u) FAIRE
            d(u) = temp;
            p(u) = u*;
```