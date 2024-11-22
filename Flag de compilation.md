---
name: Flag de compilation
type: Matière
---
#GLO-2100 

Les flag de compilation sont des spécification pour le compilateur afin d'optimiser le code et le rendre plus rapide ou plus léger aux besoin.

### Flag d'optimisation
---
Les flag d'optimisation sont les droit donné aux compilateur pour qu'il simplifie le code.
```
-O0    # Aucune optimisation
-O1    # Optimisation de base
-O2    # Optimisation supplémentaire (Est le plus courant)
-O3    # Optimisation maximal
-Os    # Optimisation pour la taille
-Ofast # Optimisation pour la vitesse d'execution
```

### Flag sécurité
---
Les drapeau de sécurité permette de spécifier les message qui vont être visible
```
-Wall      # Tous les warning
-Wextra    # Message supplémantaire
-Werror    # Les avertissement seront des erreur
-pdantic   # Conforme aux norme
-g         # Permet de spécifier un débauger externe
```

### Autre flag
---
Voir la documentation du compilateur...
