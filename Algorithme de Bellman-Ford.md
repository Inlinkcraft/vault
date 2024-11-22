---
name:
type: Matière
---
#GLO-2100 

L'algorithme de Bellman-Ford permet comme [[Algorithme de Dijkstra|algorithme de Dijkstra]] de trouver le chemin le plus cours par contre celui-ci peut avoir des poids négatif dans le [[Graph|graph]] l'algorithme détecte les cycle négatif.

### Implémentation
---
```pseudocode
POUR TOUT v DANS S FAIRE
    d(v) = INF;
    p(v) = NIL;
d(s) = 0;
RÉPÉTÉ |S| - 1 FOIS
    POUR TOUT (u, v) DE A FAIRE
        temp = d(u) + w(u, v);
        SI temp < d(v) FAIRE
            d(v) = temp;
            p(v) = u;
POUR TOUT (u, v) de A FAIRE
    SI d(v) > d(u) + w(u, v) FAIRE
        RETURN faux // Erreur cycle négatif
RETURN vrai
```

### Optimisation
---
Avec un [[Graph|graph]] orienté acyclique et [[Tri-topologique|trier topologiquement]]:
```pseudocode
POUR TOUT v DANS S FAIRE
    d(v) = INF;
    p(v) = NIL;
d(s) = 0;
(b, T) = TriTopologique(G);

SI b == faux FAIRE
    RETOUR faux;
    

POUR i = 1 à |S| FAIRE
    u = T[i]
    POUR TOUT v VOISIN DE u FAIRE
        temp = d(u) + w(u, v)
        SI temp < d(v)
            d(v) = temp
            p(v) = u
RETOUR vrai;
```

