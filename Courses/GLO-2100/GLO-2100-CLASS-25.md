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
		- ACTIVE: si cettre entrée contiennt une clé valide
		- DELETED: si cette entré a déjà contenu une cle mais que celle-ci retirée par la suite avec une opération enlever(x)
		- EMPTY: si cette entrée est vide et n'a jamais contenu une clé
- Sondage linéaire
	- Le sondage f utilisé est linéairement, i,.e. f(i) = i
		- signifie qu'après...
		- ...
- Le sondage quadratique
	- utilisé f(i) = i^2
	- ...
- Analyse du sondage quadratique
	- Démontron s qu'on est assuré de trouver une position vacante dans la table lorsque celle-ci est au moins à moitié vidence
		- On re-hachera la table lorsque l'insertion d'un élément nous donne une table avec moin de la moitié de ses cases dans l'état EMPTY
		- ..
- Double hachage
	- consiste à calculer séquentiellement le position position $h_{0}$ ... avec $h_{i} = (h(x) + f(i)) \mod{N}$ avec f(i) = i \times h'(x) ou h'(x) est une seconde fonction de hachage.
		- éviter d'avoir h'(x) = 0 (ex: h'(x) = c(x) mod R pour R < N)
			- Tous les x tels que h'(x) = 0 produiront h_0(x) = h_

---
# En retrospective