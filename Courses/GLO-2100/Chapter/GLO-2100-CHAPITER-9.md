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