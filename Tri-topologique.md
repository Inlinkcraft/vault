---
name: Tri-topologique
type: Matière
---
#GLO-2100 

Le tri-topologique permet de trier un [[Graph|graph]] selon les source, puit et arrêté d'entré et sortie

### Implémentation
---
```pseudocode
AE[1 à |S|] // Tableau des arrité d'entré de chaque sommet
Q = {};
POUR TOUT v DANS S FAIRE
    SI AE[v] == 0 FAIRE
        Q.ENFILE(v);
SI Q == {} FAIRE
    RETOUR faux // cylce détecté
i = 0;
TANT QUE Q != {} FAIRE
    u = Q.défile();
    T[++i] = u;
    POUR TOUT v VOISIN DE u FAIRE
        AE[v]--;
        SI AE[v] == 0:
            Q.ENFILE(v);
SI i != |S| FAIRE
    RETOUR FAUX // cycle
RETOUR VRAI
```

