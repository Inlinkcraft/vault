---
name: Méthode d'analyse par la transformation de Laplace
type: Matière
---
#GEL-1000 
***
Méthode pour analyser un [[Circuit électrique|circuit]] à l'aide de la [[Transformation de Laplace|transformation de Laplace]]

### Analyse général
---
1. Transformer le circuit du domaine temps vers le domaine s. ([[Composante transformer en domaine Laplace]]) 
2. Établir les équations d'équilibre en utilisant les méthodes habituelles. Les équations obtenues sont des équations algébriques. ([[Manipulation de circuit à domaine de Laplace]])
3. Résoudre les équations d'équilibre dans le domaine s et déterminer la réponse désirée.
4. Effectuer la transformée de Laplace inverse de la réponse en s, pour obtenir la réponse dans le domaine temporel. ([[Transformation de Laplace inverse]])
([[Chapitre-6.pdf#page=60&selection=0,0,8,44&color=yellow|Chapitre-6, p.60]])

### Analyse nodale
---
- L'analyse nodale fournit des tensions à tous les nœuds d'un circuit donné. Si une source de tension est connectée entre un nœud et la masse, la tension du nœud est déjà connue et nous n'avons pas besoin de trouver la tension de ce nœud.
- L'analyse nodale s'applique au circuit transformé de Laplace. Tous les éléments du circuit sont représentés dans le domaine s. Les entrées et sorties sont représentées par leurs transformées de Laplace dans le domaine s. 
- Les expressions du domaine temporel sont obtenues en prenant les transformations de Laplace inverses des expressions du domaine s.
- Cette méthode peut être utilisée pour trouver la réponse d'un circuit pour un signal d'entrée arbitraire tant que l'intégrale de Laplace du signal d'entrée converge.

> [!summary] Bref
> La même chose que les la lois de nœud.
([[Chapitre-6.pdf#page=61&selection=0,30,27,25&color=yellow|Chapitre-6, p.61]])

### Analyse des mailles
---
- L'analyse des mailles fournit des courants circulatoires dans toutes les mailles du circuit. À partir de ces courants, nous pouvons trouver des courants dans chaque branche. Si une maille contient une source de courant, le courant de maille est le même que le courant de la source de courant s'ils pointent dans la même direction. Si la direction est opposée, le courant de maille est le négatif du courant provenant de la source de courant. 
- L'analyse des mailles s'applique au circuit transformé de Laplace. Tous les éléments sont alors représentés dans le domaine s. Les signaux d’entrées et sorties sont représentés par leurs transformées de Laplace. 
- Les expressions du domaine temporel sont obtenues en prenant les transformée de Laplace inverses des expressions du domaine s. 
- Cette méthode peut être utilisée pour trouver la réponse d'un circuit pour une entrée arbi

> [!summary] Bref
> La même chose que la lois des maille

([[Chapitre-6.pdf#page=63&selection=0,0,29,20&color=yellow|Chapitre-6, p.63]])

### Équivalent Thévenin
---
- La Figure 15.40 montre un circuit avec une paire de bornes a et b. Si le circuit est un circuit transformé de Laplace constitué d'impédances et de sources dans le domaine s, il peut être représenté par une source en série avec une impédance comme le montre la Figure 15.41. 
- La tension équivalente de Thévenin V th(s) est obtenue en trouvant la tension en circuit ouvert entre a et b à partir du circuit d'origine, comme le montre la Figure 15.42. 
 - Méthode du test
([[Chapitre-6.pdf#page=65&selection=0,45,20,17&color=yellow|Chapitre-6, p.65]])

#### Équivalent Norton
---
- La Figure 15.57 montre un circuit avec une paire de bornes a et b. Si le circuit est un circuit transformé de Laplace constitué d'impédances et de sources dans le domaine s, le circuit peut être représenté par une source de courant et une impédance parallèle comme le montre la Figure 15.58. Cette représentation est appelée circuit équivalent Norton.
- Le courant équivalent de Norton I N(s) est obtenu en trouvant le courant de court-circuit entre a et b du circuit d'origine, comme le montre la Figure 15.59. 
- L'impédance équivalente Norton est trouvée en utilisant les mêmes méthodes que celles utilisées pour trouver l'impédance équivalente de Thévenin.
([[Chapitre-6.pdf#page=68&selection=0,0,26,12&color=yellow|Chapitre-6, p.68]])