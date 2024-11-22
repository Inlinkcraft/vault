---
name: Algorithme de Kosaraju
type: Matière
---
#GLO-2100 

L'algorithme de Kosaraju permet de trouver les composante fortement connexe d'un [[Graph|graph]].

### Implémentation
---
```pseudocode
GI = Inverse(G);
Q = ParcoursProfondeur(GI);
C = {};
POUR TOUT s DE G: visité[s] = faux;
TANT QUE Q != {} FAIRE
    k = Q.DEPILER();
    SI visité[k] == faux FAIRE:
        Z = {};
        explore(k, G); ()
        C = C.Ajouter(Z)
retourner C
```