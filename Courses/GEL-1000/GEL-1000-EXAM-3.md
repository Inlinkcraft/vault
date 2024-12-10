---
name: Examen-3
type: Evaluation
course: GEL-1000
date: 2024-12-10T08:30
ponderation: 35
note:
status: En cours
---
#school/GEL-1000  

### Structure de l'examen
---
1. Circuit LC Source commander Laplace
    - [x] Méthode des noeud
    - [x] Méthode des maille
    - [x] Valeur finale
2. Circuit d'ordre 2 condition initial avec différentielle
    - [x] Bonnus coefficient d'ammortissement pour le comportement
3. Circuit la fonction de transfer avec apli-op (Passe/filtre)
    - [x] Question à dévelopmment
4. Fonction de transfert Laplace / inverse
    - [ ] 2 Questions ?
5. Calculer le décalage ? Transformation de réponse
6. Circuit RL du premier ordre Laplace

### Études
---

##### Question 3:
![[Chapitre-6.pdf#page=93&rect=102,78,321,782|Chapitre-6, p.93]]
```circuitjs
$ 1 0.000005 45.7144713268909 45 5 50 5e-11
a 800 368 944 368 8 15 -15 1000000 0 0 100000
r 656 352 720 352 0 25
g 656 448 656 464 0 0
g 944 448 944 464 0 0
r 944 448 944 368 0 1000000
v 656 448 656 352 0 1 1702.64 5 0 0 0.5
g 720 448 720 464 0 0
g 800 448 800 464 0 0
r 800 352 800 272 0 1000
c 720 352 720 272 0 0.00001 0.001 0.001
c 720 352 800 352 0 0.00001 0.001 0.001
w 720 272 800 272 0
w 800 272 944 272 0
w 944 272 944 368 0
w 800 384 800 448 0
r 720 352 720 448 0 1000
38 5 F1 3 4 5000 -1 Frequency
```
