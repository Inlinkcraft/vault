---
name: Arbre rouge et noir
type: Chapter
course: GLO-2100
---

Arbres rouge et noir
---
> [!todo] Motivation
> - Limitation des arbres AVL
> 	- Il faut stocker l'information de hauteur dans les noeud
> 	- La récursivité implique de remonter jusqu'à la racine
> 	- En pratique, d'autre aooriches sont plus rapides, comme les arbre rouge et noir dont l'insertion et le retraut se dont treaverse lM'a...
### Propriété
---
- Arbre binaire ordonné. 
- Chaque noeud est rouge ou noir. 
- La racine est noire. 
- Les feuilles (pointeurs NULL) sont noires. 
- Les enfants d’un noeud rouge sont noirs. 
- À partir de n’importe quel noeud, tous les chemins de la racine jusqu’à un pointeur NULL doivent avoir le même nombre de noeuds noirs
([[Chapitre-9.pdf#page=3&selection=12,0,116,5&color=yellow|Chapitre-9, p.3]])

> [!attention] Remarque
> - Comme la racine est noire et il ne peut y avoir plus de deux noeuds rouges consécutifs, la longueur de tout chemin de la racine à une feuille ne peut être supérieure à 2 fois le nombre de noeuds noirs dans ce chemin. 
> - La hauteur d’un arbre rouge et noir est maximum 2𝑙𝑜𝑔! 𝑛 + 1 .
([[Chapitre-9.pdf#page=4&selection=16,0,46,1|Chapitre-9, p.4]])
### Exemple
---
![[Chapitre-9.pdf#page=5&rect=147,45,818,452|Chapitre-9, p.5]]
##### Erreur deux nœud rouge

### Insertions
---
### Suppression
---