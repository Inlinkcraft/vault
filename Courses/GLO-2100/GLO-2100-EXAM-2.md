---
name: Examen finale
type: Evaluation
course: GLO-2100
date: 2024-12-15T09:00
ponderation: 35
note:
status: "À Faire"
---
#school/GLO-2100 


### Plan d'étude

- [x] Fonction de hachage
- [x] Gestion  des collisions
    - [x] Chaînage externe
    - [x] Adressage ouvert
        - [x] Sondage linéaire
        - [x] Sondage quadratique
        - [x] Double hachage
- [x] Hachage universel
- [x] Terminologie des arbres
- [x] Parcours d'arbres
    - [x] Pré-ordre
    - [x] Post-ordre
    - [x] En-ordre
- [x] Implémentation des arbres dans un tableau
    - [x] Implémentation par chaînage
- [x] Monceaux
    - [x] Tri par tas ("Heap sort")
- [ ] Arbre binaire de recherche
    - [ ] Peuvent être utilisés pour implémenter les dictionnaires
    - [ ] Dictionnaire: conteneur d'élément devant supporter efficacement les opérations suivante:
        - [ ] Insertion d'un élément
        - [ ] Suppression d'un élément
        - [ ] Trouver un élément (déterminer si un élément est présent)
    - [ ] s'effectuent en $O (\log(n))$ lorsque l'arbre de n élément est équilibré
- [ ] Arbre AVL
    - [x] un arbre binaire de recherche (de tri) doit être équilibré pour supporter efficacement les opérations de recherche, d'insertion et de suppression
    - [x] Le facteur d'équilibre d'un noeud est de k lorsque:
        - [x] |hauteur(sous-arbre droit)- hauteur(sous-arbre gauche)| = k
        - [x] Remarque: La hauteur d'un arbre de 0 noeud est  -1
    - [ ] Un arbre est $HB[k]$ lorsque le facteur d'équilibre de ses noeuds est $\le$ k
    - [ ] Noeud critique
    - [ ] Déséquilibre
        - [ ] Trouver les cas de déséquilibre
            - [ ] ZigZigGauche
            - [ ] ZigZigDroit
            - [ ] ZigZagDroit
            - [ ] ZigZagGauche
    - [ ] Retirer
    - [ ] Recherche
- [ ] Arbre rouge et noir
    - [ ] Propriétés
        - [ ] Arbre binaire ordonné
        - [ ] Noeud rouge ou noir seulement
        - [ ] La racine est noir
        - [ ] Les feuille sont null et noir
        - [ ] Les enfant d'un noeud rouge sont noir
        - [ ] à partir de n'importe quel noeud, tous les chemins de la racine jusqu'à un pointeur NULL doivent avoir le même nombre de noeuds noir.
    - [ ] Exemples
    - [ ] insertions
        - [ ] 3 Cas
    - [ ] Supressions
        - [ ] Supprimer le noeud à la bonne position comme dans un arbre AVL
        - [ ] Ensuite, on doit gérer le coloriage et le balancement
        - [ ] 3 cas de la suppression et 6 pour fixer le coloriage