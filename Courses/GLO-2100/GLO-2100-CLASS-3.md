---
name: Cours-3
type: Class
course: GLO-2100
date: 2024-09-12T10:30
status: "Compléter"
---
#school/GLO-2100 
***

# Chapitre 2

## Qualité du code
Un code de qualité se doit d'être:
- Fonctionnel
- Fiable
- Convivial
- Efficace ==Exploré fortement dans le cours==
- Maintenable
- Portable

> [!Info] AKA
> "ça compile" n'est pas suffisant

## Norme et pratique

### Théorie des contrat
Retours sur la [[Théorie des contrat]] à l'aide des macros fournie par le professeur.

### Test unitaire
Pour valider les resultât de notre code d'avantage il est possible d'utilisé des code unitaire comme [Google Test](https://github.com/google/googletest).

### Doxygen
Doxygen permet de documenter sont code en c++.

### Classe
Une classe se doit d'être valide t'en qu'elle existe

### Fonction
La référence constante évite les copie donc elle est plus efficace. Par contre si la référence est modifier par la fonction cela n'est pas possible.
Une référence qui est retourné se doit toujours d'être constante pour forcer une copy pour éviter de perdre la valeur.

## Surcharge des deux opérateur d'incrémentation
Dans un but d'optimisation nous avons exploré plus en detail les deux [[Surcharge#Surcharge de l'opérateur d'incrémentation|opérateur d'incrémentation]] pour constater que l'un d'entre eux est plus efficace que le l'autre. 

## Templates
Les [[Template|templates]] permet de généraliser un type dans une classe

## Smart pointers
Les [[Smart pointer|smart pointers]] permette de généré plus facilement les pointer à partir de C++14.

## lvalue / rvalue
[[l-r values]] est un concept un peu abstrait qui consiste a séparé chaque commande d'assosiation en deux "zone".

## Introduction aux foncteur
Un [[Foncteur|foncteur]] est n objet qui encapsule une fonction. Un foncteur peut contenir des état ou des valeurs considérant que ces un objet. Plusieurs [[Foncteur|foncteurs]] sont donné par cpp dans la librairy `#include <Predicat>`.