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
L'analyse nodale s'applique au [[Circuit électrique|circuit]] [[Transformation de Laplace|transformé de Laplace]]. Tous les éléments du [[Circuit électrique|circuit]] sont représentés dans le domaine s. Les entrées et sorties sont représentées par leurs [[Transformation de Laplace|transformées de Laplace]] dans le domaine s. Les expressions du domaine temporel sont obtenues en prenant les [[Transformation de Laplace inverse|transformations de Laplace inverses]] des expressions du domaine s. ([[Chapitre-6.pdf#page=61&selection=12,1,21,65&color=yellow|Chapitre-6, p.61]])

1.  [[Composante transformer en domaine Laplace]] 
2. Appliquer la [[Méthode des nœud|méthode des nœud]].
3. [[Transformation de Laplace inverse]]

> [!summary] Bref
> La même chose que les la [[Méthode des nœud|méthode des nœud]] dans le domaine temporel.

### Analyse des mailles
---
L'analyse des mailles s'applique au [[Circuit électrique|circuit]] [[Transformation de Laplace|transformé de Laplace]]. Tous les éléments sont alors représentés dans le domaine s. Les signaux d’entrées et sorties sont représentés par leurs [[Transformation de Laplace|transformées de Laplace]]. Les expressions du domaine temporel sont obtenues en prenant les [[Transformation de Laplace inverse|transformée de Laplace inverses]] des expressions du domaine s. ([[Chapitre-6.pdf#page=63&selection=16,0,24,61&color=yellow|Chapitre-6, p.63]])

1.  [[Composante transformer en domaine Laplace]] 
2. Appliquer la [[Méthode des maille|méthode des maille]].
3. [[Transformation de Laplace inverse]]

> [!summary] Bref
> La même chose que la [[Méthode des maille|méthode des maille]] dans le domaine temporel

### Équivalent Thévenin
---
La tension équivalente de [[Théorème de Thévenin|Thévenin]] $V_{th}(s)$ est obtenue en trouvant la [[Tension électrique|tension]] en [[Circuit électrique|circuit]] ouvert entre les borne à partir du [[Circuit électrique|circuit]] d'origine. ([[Chapitre-6.pdf#page=65&selection=11,0,15,68&color=yellow|Chapitre-6, p.65]]) 

> [!note] La résistance est remplacer
> Trois méthodes pour trouver l'impédance équivalente de Thévenin $Z_{th}(s)$:
> 1. Trouver le courant de court-circuit $I_{sc}(s)$ entre les bornes:
> $$Z_{th} = \frac{V_{th}(s)}{I_{sc}(s)}$$
> 2. Désactiver les [[Source indépendante|sources indépendantes]] dans le [[Circuit électrique|circuit]] en court-circuitant les sources de [[Tension électrique|tension]] et en ouvrant les sources de [[Courant électrique|courant]]. Ensuite, trouvez l'[[Impédance|impédance]] équivalente vue des bornes. 
> > [!attention] 
> > Cette méthode ne peut pas être utilisée si le circuit contient des sources dépendantes.
> 
> 3. Expérimental
> ([[Chapitre-6.pdf#page=65&selection=20,0,21,7&color=yellow|Chapitre-6, p.65]])

#### Équivalent Norton
---
Le courant équivalent de [[Théorème de Norton|Norton]] $I_{N}(s)$ est obtenu en trouvant le [[Courant électrique|courant]] de court-circuit entre les bornes du [[Circuit électrique|circuit]] d'origine. ([[Chapitre-6.pdf#page=68&selection=14,1,19,58&color=yellow|Chapitre-6, p.68]])

> [!note] La résistance est remplacer
> Trois méthodes pour trouver l'impédance équivalente de Norton $Z_{N}(s)$:
> 1. Trouver la tension de circuit-ouvert $V_{co}(s)$ entre les bornes:
> $$Z_{N} = \frac{V_{co}(s)}{I_{N}(s)}$$
> 2. Désactiver les [[Source indépendante|sources indépendantes]] dans le [[Circuit électrique|circuit]] en court-circuitant les sources de [[Tension électrique|tension]] et en ouvrant les sources de [[Courant électrique|courant]]. Ensuite, trouvez l'[[Impédance|impédance]] équivalente vue des bornes. 
> > [!attention] 
> > Cette méthode ne peut pas être utilisée si le circuit contient des sources dépendantes.
> 
> 3. Expérimental
> ([[Chapitre-6.pdf#page=65&selection=20,0,21,7&color=yellow|Chapitre-6, p.65]])