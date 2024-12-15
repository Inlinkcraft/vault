---
name: Arbre rouge et noir
type: Chapter
course: GLO-2100
---
/
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
![[Chapitre-9.pdf#page=6&rect=79,48,834,435|Chapitre-9, p.6]]

> Le noeud 90 et 95 se touche et il sont tous les deux rouge...

##### Erreur pas le même nombre de nœud noir entre deux branche
![[Chapitre-9.pdf#page=7&rect=52,36,818,436|Chapitre-9, p.7]]

### Insertions
---
**3 cas possible pour l'Insertion**
Nous avons:
- x (le noeud)
- père de x
- frère de x
- grand-père de x
- oncle de x
##### Insertion rouge-noir
```c++
void insertionRougeNoir(int valeur)
{
	Noeud* noeud = new Noeud;
	noeud -> data = valeur;
	noeud -> parent = null_ptr;
	noeud -> gauche = *feuille;
	noeud -> droit = *feuille;
	noeud -> couleur = Rouge
	
	Noeud* y = null_ptr;
	Noeud* x = *racine;
	
	Tant que (x != *feuille){
		y = x;
		si (noeud -> data < x -> data){
			x = x -> gauche;
		}
		else
		{
			x = x -> droit;
		}
	}
	
	noeud -> parent = y;
	
	Si (y = null_ptr)
	{
		racine = noeud;
	}
	Sinon
	{
		Si (noeud -> data < y -> data)
			y -> gauche = noeud;
		Sinon
			y -> droit = noeud;
	}
	
	Si (noeud -> parent == null_ptr)
	{
		noeud -> couleur = noir;
		return;
	}
	
	Si (noeud -> parent -> parent == null_ptr)
	{
		return;
	}
	
	insertionColoriage(noeud);
	
}
```

```c++
void insertionColoriage(Noeud& noeud){
	Tant que (noeud -> parent -> couleur == rouge)
	{
		Si (noeud -> parent == [(noeud -> parent) -> parent] -> droit)
		{
			u = [(noeud -> parent) -> parent] -> gauche;
			Si (u -> couleur == rouge)
			{
				u -> couleur = noir;
				noeud -> parent -> couleur = noir;
				[(noeud -> parent) -> parent] -> couleur = rouge;
				noeud = noeud -> parent -> parent;
			}
			Sinon
			{
				Si (noeud == noeud -> parent -> gauche)
				{
					noeud = noeud -> Parent;
					_ZigZigGauche(noeud);
				}
				noeud -> parent -> couleur = noir;
				noeud -> parent -> parent -> couleur = rouge
				_ZigZigDroit(noeud -> parent -> parent);
			}
		}
		Sinon (noeud -> parent == [(noeud -> parent)-> parent] -> gauche)
		{
			u = [(noeud -> parent) -> parent] -> droit;
			Si (u -> couleur == rouge)
			{
				u -> couleur = noir;
				noeud -> parent -> couleur = noir;
				[(noeud -> parent) -> parent] -> couleur = rouge;
				noeud = noeud -> parent -> parent;
			}
			Sinon
			{
				Si (noeud == noeud -> parent -> droit)
				{
					noeud = noeud -> parent;
					_ZigZigDroit(noeud);
				}
				noeud -> parent -> couleur = noir;
				noeud -> parent -> parent -> couleur = rouge;
				_ZigZigGauche(noeud -> parent -> parent)
			}
		}
	}
}
```

### Suppression
---
- Supprimer le noeud à la bonne position comme dans un arbre AVL. 
- Ensuite, on doit gérer le coloriage et le balancement. 
- On verra 3 cas pour la suppression et 6 pour fixer le coloriage
([[Chapitre-9.pdf#page=93&selection=6,0,50,0&color=yellow|Chapitre-9, p.93]])

![[Chapitre-9.pdf#page=94&rect=135,113,783,447&color=yellow|Chapitre-9, p.94]]

##### Cas 1: Supression à deux feuilles comme enfant
1. On suprime et remplace par un `null_ptr`

##### Cas 2: Supression à une feuille comme enfant
1. On suprime le noeud et on le remplace par sont enfant unique

##### Cas 3:  Supression à deux noeud interne
1. Comme pour les arbres AVL, il faut donc d’abord retrouver son successeur minimal à droite à l’aide d’une boucle simple (une fois à droite, plein de fois à gauche).
2. Ensuite, on doit les échanger et on supprime le noeud
([[Chapitre-9.pdf#page=97&selection=24,0,80,0&color=yellow|Chapitre-9, p.97]])

> [!attention]  Réparé les propriété
> - Lorsqu’on fait ce changement et qu’on supprimer un noeud, il se peut que certaines propriétés de l’arbre rouge-noire soit violées. 
> - Il faut faire des changements pour respecter ces propriétés. 
> - On verra plusieurs cas. 
> - Noter que dans tous les cas, le noeud supprimé aura 0 ou 1 enfant, puisque dans le cas où il y avait deux enfants, nous avons fait un changement de noeud.
([[Chapitre-9.pdf#page=102&selection=12,0,122,1&color=yellow|Chapitre-9, p.102]])

##### Réparation des propriété
###### Cas 1:
- 𝑥 ou 𝑏 est rouge (comme on ne peut pas avoir deux noeuds consécutifs rouge, on au maximum un des deux noeuds rouges)
- Dans ce cas, on remplace la couleur de l’enfant par noir. Ici, le noeud contenant 5 devient donc noir.
([[Chapitre-9.pdf#page=104&selection=18,0,49,7&color=yellow|Chapitre-9, p.104-105]])

###### Cas 2:
- Les deux noeuds sont noirs. 
- Dans ce cas, retirer un noeud enlève un noeud noir du chemin. On doit donc fixer la propriété pour ramener deux noeuds noirs sur chaque chemin. 
- On verra plusieurs sous-cas : 
	- Si 𝑥 est la racine 
		Si le noeud 𝑥 est devenu la racine, on recolorie la racine en noir ([[Chapitre-9.pdf#page=107&selection=24,0,47,3&color=yellow|Chapitre-9, p.107]])
	- Si 𝑓 est noir et ses enfants sont rouges. 
		Résolution :
		 - Supprimer x 
		 - Rebalancement #1 
			 - 𝑓 est à droite de 𝑏 
				 - On rebalance en faisant un ZigZigDroit sur 𝑟. 
			 - 𝑓 est à gauche de 𝑏 
				 - On rebalance en faisant un ZigZigGauche sur 𝑟. 
		- colorier 𝑟 en noir
		([[Chapitre-9.pdf#page=108&selection=30,0,81,4&color=yellow|Chapitre-9, p.108]])
	- Si 𝑓 est noir un de ses enfants est rouge. 
		Résolution
		- Supprimer x
		- Rebalancement #1
			- f est à droite de b et le noeud rouge est l
				- on rebalance en fesant un zigzagDroit sur B
			- f est à gauche de b et le noeud rouge est l
				- on rebalance en fesant un zigzagGauche sur B
			- colorier l en noir
	> On peut mettre les deux cas 𝑏 et 𝑐 dans le même cas et faire un ZigZig si le noeud rouge est à la bonne position.
	
	- Si 𝑓 est noir et ses enfants sont noirs. 
		- Résolution 
			- Supprimer x 
			- Rebalancement #1 
				- 𝑓 est à droite de 𝑏 ü 
				- On colorie 𝑓 rouge 
			- Si 𝑏 est noir, on refait les cas de supressions pour 𝑏 tant que 𝑏 est noir. 
			- Si b est rouge, on le colorie noir.
		([[Chapitre-9.pdf#page=140&selection=30,0,106,5&color=yellow|Chapitre-9, p.140]])
	- Si 𝑓 est rouge
		- Résolution 
			- Supprimer x. 
			- Rebalancement #1 
				- 𝑓 est à droite de 𝑏 
				- On rebalance en faisant un ZigZigDroit sur 𝑏. 
			- Colorier 𝑓 noir 
			- Colorier 𝑙 rouge
			([[Chapitre-9.pdf#page=150&selection=22,0,79,5&color=yellow|Chapitre-9, p.150]])
([[Chapitre-9.pdf#page=106&selection=14,0,155,5&color=yellow|Chapitre-9, p.106]])


Synthèse
---
- Arbre rouge et noir plus complexe que AVL 
- Moins de rotations que les arbres AVL 
- Recherche plus longue pour red-black (l’arbre peut être un peu plus débalancé que AVL)
([[Chapitre-9.pdf#page=162&selection=6,0,53,4&color=yellow|Chapitre-9, p.162]])