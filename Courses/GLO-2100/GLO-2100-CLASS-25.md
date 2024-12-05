---
name: Cours-25
type: Class
course: GLO-2100
date: 2024-12-05T10:30
status: Cette semaine
---
#school/GLO-2100 
***
# Avant le cour
## Plan de cours
- 

## Todo
- 

---
# Matière abordée

- 

## Notes supplémentaire

- Chapitre 6
	- Fonction de hachage
	- Gestion de collisions
		- Chaînage externe
		- Adressage ouvert
			- Sondage linéaire
			- Sondage quadratique
			- Double hachage
	- Hachage universelle
- Table de dispersion (pour dictionnaires)
	- Conteneur non ordonnées
	- Insertion, Supression, Trouver un élément
		- presque toujours en O(1)
	- ... (voir les slides il va trop vite)
	- on utilise un tableau listeChaque liste contient les clef qui hachent à la même valeur d'Index
	- h(x) nous donne la lister à utiliser pour trouver(x), enlever(x) et ajouter(x)
	- Pour le cas d'un map:Chaque noeud contient une paire (clef, valeur)
	- Avec h(x) = x mod 10 pour des clef x des entiers non signés
- Taux d'occuoation pour hachage externe
	- Pour éciter d'avoir de longue listes chainées
		- On augmente la taille de la table de dispersion aussitot que le nombre n ...
		- ...
		- Supposins une fonction de hachage idéale distribuant les clef vers tous les indexes possibles (i.e. le meilleur cas)
		- ...
- Gestion des colision
	- Chainage externe
			- tableau de liste 
			- hx  donne la liste a utilisé
		- implémentation
			- hashf calcule le code de hachage
			- partie compression dans myhash
			- myhash privée
			- trouver un nombre premier
		- Taux d'occupation
			- $\lambda = \frac{2}{N}$
			- Rehash...
- Adressage ouvert
	- Problème avec le chainage externe:
		- allocation dynamique pour l'insertion dans une liste couteuse
		- avantage..
		- ...
	- Les position $h_{0}$, $h_{1}$, $h_{2}$, ... sont calculés séquentiellement
		- avec $h_i = (h(x) + f(i))  \mod{N}$
	- nécessite aussi la présence d'un champ état pour chaque entré de la table de dispertion
	- indique l'état de cette entré:
		- ACTIVE: si cettre entrée contiennt une clé vali

---
# En retrospective