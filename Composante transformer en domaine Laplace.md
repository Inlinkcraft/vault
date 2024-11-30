---
nom: Composante électrique (Laplace)
type: Matière
---
#GEL-1000 
***
Tous les [[Composante électrique|composante électrique simple]] devienne des [[Impédance|impédance]] ou une [[Admittance|admittance]].

### Transformation de source
---
La transformation de source ce fait à l'aide des [[Transformation de Laplace|transformation de Laplace]] en trouvant leur formule équivalente.

> [!info] Par convention...
> Par convention les fonction de [[Source électrique|source]] dans le domaine du temps seront noté d'une minuscule ($i(t)$, $v(t)$) par contre les [[Source électrique|source]] dans le domaine de Laplace seront des majuscule ($I(s)$, $V(s)$).
### Résistance
---
![[Résistance électrique#Représentation Laplace]]

### Condensateur
---
![[Condensateur électrique#Représentation Laplace]]
([[Chapitre-6.pdf#page=51&selection=0,30,0,30&color=yellow|Chapitre-6, p.51]])

> [!attention] 
> Une source est ajouter pour la valeur initial
> ![[Chapitre-6.pdf#page=51&rect=201,78,443,747|Chapitre-6, p.51]]
### Inductance
---
![[Inductance électrique#Représentation Laplace]]
([[Chapitre-6.pdf#page=52&selection=0,27,0,27&color=yellow|Chapitre-6, p.52]])

> [!attention] 
> Une source est ajouter pour la valeur initial
>![[Chapitre-6.pdf#page=52&rect=234,22,445,814|Chapitre-6, p.52]]

### Tableau récapitulatif
---

| Élément                     | [[Impédance]]  | [[Admittance]] |
| --------------------------- | :------------: | :------------: |
| [[Résistance électrique]]   |      $R$       | $\frac{1}{R}$  |
| [[Condensateur électrique]] |      $Ls$      | $\frac{1}{Ls}$ |
| [[Inductance électrique]]   | $\frac{1}{Cs}$ |      $Cs$      |
