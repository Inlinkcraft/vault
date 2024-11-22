---
name: Algorithme du parcours en largeur
type: Matière
---
#GLO-2100 

L'algorithme du parcours en largeur d'un graph permet comme sont nom l'indique de parcourir un [[Graph|graph]] en largeurs.

### Implémentation
---
```pseudocode
POUR TOUT u DE S: visité(u) = faux;
POUR TOUT u DE S: previous(u) = nil;
visité(v) = vrai;
Q.ENFILER(v)
TANT QUE Q != {} FAIRE
    u* = Q.DEFILE();
    POUR TOUT u VOISIN DE u*:
        IF visité(u) == false:
            visité(u) = vrai
            P(u) = u*
            Q.ENFILE(u)
```