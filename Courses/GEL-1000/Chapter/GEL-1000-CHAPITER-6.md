---
name: Analyse des circuits par la transformation de Laplace
type: Chapter
course: GEL-1000
---
#GEL-1000 
Transformation de Laplace
---
![[Transformation de Laplace]]
Théorème de la valeur initiale et la valeur final
---
![[Théorème de la valeur initiale]]
![[Théorème de la valeur finale]]
Transformation de Laplace inverse
---
![[Transformation de Laplace inverse]]

Théorème des résidu
---
![[Théorème du résidus]]

Décomposition en fraction partielle
---
![[Décomposition en fractions partielles]]

Analyse des circuits dans l'espace de Laplace
---
![[Composante transformer en domaine Laplace]]

![[Manipulation de circuit à domaine de Laplace]]

### Impédance et admittance dans l'espace de Laplace
([[Chapitre-6.pdf#page=53&selection=0,48,0,48&color=yellow|Chapitre-6, p.53]])

##### Diviseur de tension dans le domaine s
([[Chapitre-6.pdf#page=54&selection=0,0,0,37&color=yellow|Chapitre-6, p.54]])

##### Diviseur de courant dans le domaine s
([[Chapitre-6.pdf#page=55&selection=0,0,0,37&color=yellow|Chapitre-6, p.55]])

Fonctionne a condition d'utilisée l'impédence et admittance

![[Chapitre-6.pdf#page=57&rect=54,68,574,751&color=yellow|Chapitre-6, p.57]]

#### EXAMPLE 15.1
([[Chapitre-6.pdf#page=58&selection=0,0,0,12&color=yellow|Chapitre-6, p.58]])
$$V_{T}=\frac{1}{s}+1.5|_{0.5s=z_{2}}^{2\Omega=z_{1}}$$
$$V_{1}=\frac{V_{T}\times z_{1}}{z_{1}+z_{2}}$$
#### EXAMPLE 15.3
([[Chapitre-6.pdf#page=59&selection=0,0,0,12&color=yellow|Chapitre-6, p.59]])
- Addition des sources
	$$\frac{4}{s}-\frac{2}{s}+3=\frac{3s+2}{s}$$

### Méthode d'analyse par la T. de Laplace 
1. Transformer le circuit du domaine temps vers le domaine s. 
2. Établir les équations d'équilibre en utilisant les méthodes habituelles. Les équations obtenues sont des équations algébriques. 
3. Résoudre les équations d'équilibre dans le domaine s et déterminer la réponse désirée.
4. Effectuer la transformée de Laplace inverse de la réponse en s, pour obtenir la réponse dans le domaine temporel.
([[Chapitre-6.pdf#page=60&selection=0,0,8,44&color=yellow|Chapitre-6, p.60]])

#### Analyse nodale dans le domaine s 
- L'analyse nodale fournit des tensions à tous les nœuds d'un circuit donné. Si une source de tension est connectée entre un nœud et la masse, la tension du nœud est déjà connue et nous n'avons pas besoin de trouver la tension de ce nœud.
- L'analyse nodale s'applique au circuit transformé de Laplace. Tous les éléments du circuit sont représentés dans le domaine s. Les entrées et sorties sont représentées par leurs transformées de Laplace dans le domaine s. 
- Les expressions du domaine temporel sont obtenues en prenant les transformations de Laplace inverses des expressions du domaine s.
- Cette méthode peut être utilisée pour trouver la réponse d'un circuit pour un signal d'entrée arbitraire tant que l'intégrale de Laplace du signal d'entrée converge.

> [!summary] Bref
> La même chose que les la lois de nœud.

([[Chapitre-6.pdf#page=61&selection=0,30,27,25&color=yellow|Chapitre-6, p.61]])

#### Analyse des mailles dans le domaine s 
- L'analyse des mailles fournit des courants circulatoires dans toutes les mailles du circuit. À partir de ces courants, nous pouvons trouver des courants dans chaque branche. Si une maille contient une source de courant, le courant de maille est le même que le courant de la source de courant s'ils pointent dans la même direction. Si la direction est opposée, le courant de maille est le négatif du courant provenant de la source de courant. 
- L'analyse des mailles s'applique au circuit transformé de Laplace. Tous les éléments sont alors représentés dans le domaine s. Les signaux d’entrées et sorties sont représentés par leurs transformées de Laplace. 
- Les expressions du domaine temporel sont obtenues en prenant les transformée de Laplace inverses des expressions du domaine s. 
- Cette méthode peut être utilisée pour trouver la réponse d'un circuit pour une entrée arbi

> [!summary] Bref
> La même chose que la lois des maille

([[Chapitre-6.pdf#page=63&selection=0,0,29,20&color=yellow|Chapitre-6, p.63]])

#### Circuit équivalent Thévenin dans le domaine s
- La Figure 15.40 montre un circuit avec une paire de bornes a et b. Si le circuit est un circuit transformé de Laplace constitué d'impédances et de sources dans le domaine s, il peut être représenté par une source en série avec une impédance comme le montre la Figure 15.41. 
- La tension équivalente de Thévenin V th(s) est obtenue en trouvant la tension en circuit ouvert entre a et b à partir du circuit d'origine, comme le montre la Figure 15.42. 
 - Méthode du test
([[Chapitre-6.pdf#page=65&selection=0,45,20,17&color=yellow|Chapitre-6, p.65]])

#### Circuit Norton équivalent dans le domaine s 
- La Figure 15.57 montre un circuit avec une paire de bornes a et b. Si le circuit est un circuit transformé de Laplace constitué d'impédances et de sources dans le domaine s, le circuit peut être représenté par une source de courant et une impédance parallèle comme le montre la Figure 15.58. Cette représentation est appelée circuit équivalent Norton.
- Le courant équivalent de Norton I N(s) est obtenu en trouvant le courant de court-circuit entre a et b du circuit d'origine, comme le montre la Figure 15.59. 
- L'impédance équivalente Norton est trouvée en utilisant les mêmes méthodes que celles utilisées pour trouver l'impédance équivalente de Thévenin.
([[Chapitre-6.pdf#page=68&selection=0,0,26,12&color=yellow|Chapitre-6, p.68]])

## Fonction de transfert 
- Dans le circuit transformé de Laplace avec des ==conditions initiales nulles==, le rapport de la sortie dans le domaine s à l'entrée dans le domaine s est défini comme la fonction de transfert. 
- Soit X(s) la représentation du domaine s de l'entrée, et soit Y(s) la représentation du domaine s de la sortie. La fonction de transfert est alors: 
- $$H(s)=\frac{Y(s)}{X(s)}\sim \frac{V_{out}}{V_{in}}$$
> [!note] $H(s)$
> $H(s)$ est "ADN" du système
> Se nomme la "Fonction réseau"
- L'entrée peut être une tension ou un courant, et la sortie peut être une tension ou un courant. La ou les sorties Y peuvent être écrites sous la forme $$Y(s) = H(s)X(s)$$
- La fonction de transfert $H(s)$ transfère l'entrée $X(s)$ vers la (les) sortie(s). Dans le processus de transfert, le signal d'entrée est modifié. La nature de la modification est spécifiée dans la fonction de transfert. 
- La fonction de transfert $H(s)$ représente les effets du circuit (ou du système en général) sur le(s) signaux $X(s)$ d'entrée.
([[Chapitre-6.pdf#page=70&selection=0,0,29,41&color=yellow|Chapitre-6, p.70]])

![[Chapitre-6.pdf#page=71&rect=432,169,569,641&color=yellow|Chapitre-6, p.71]]

![[Chapitre-6.pdf#page=72&rect=324,80,557,778&color=yellow|Chapitre-6, p.72]]

| Fonction de réseau    |                         | $H(s)$                             |
| --------------------- | ----------------------- | ---------------------------------- |
| Immitance             | Impédance               | $Z_1(s)=\frac{V_{1}(s)}{I_{1}(s)}$ |
|                       | Admittance              | $Y_1(s)=\frac{I_{1}(s)}{V_{1}(s)}$ |
| Fonction de transfert | Impédance de transfert  | $Z_1(s)=\frac{V_{1}(s)}{I_{1}(s)}$ |
|                       | Admittance de transfert | $Z_1(s)=\frac{V_{1}(s)}{I_{1}(s)}$ |
|                       | Gain en tension         | $Z_1(s)=\frac{V_{1}(s)}{I_{1}(s)}$ |
|                       | Gain en courant         | $Z_1(s)=\frac{V_{1}(s)}{I_{1}(s)}$ |

##### Réponse à l’impulsion, réponse à l’échelon, réponse à la rampe
- La fonction de transfert H(s) masque les détails du circuit et décrit mathématiquement les effets du circuit sur le signal d'entrée. Le circuit donné peut maintenant être représenté comme une boîte noire avec H(s) comme le montre la Figure 15.71. 
- La sortie y(t) est obtenue en prenant la transformée de Laplace inverse de Y(s), c'est-à-dire y(t) = L-1[Y(s)] = L-1[H(s)X(s)]. 
- Réponse impulsionnelle: x(t) = (t). X(s) = 1. Y(s) = H(s)1 = H(s). h(t) = L1[H(s)] 
- Réponse à l'échelon: x(t) = u(t). X(s) = 1/s. Y(s) = H(s)/s. h s(t) = L1[H(s)/s] 
- Réponse à la rampe: x(t) = tu(t). X(s) = 1/s 2. Y(s) = H(s)/s 2. h r (t) = L1[H(s)/s2

La fonction de transfert peut être écrite sous forme factorisée comme suit : 

où p1, p2, ….., pn sont des pôles, z 1, z 2, ….., zm sont des zéros, et K est une constante.
([[Chapitre-6.pdf#page=75&selection=21,0,40,14&color=yellow|Chapitre-6, p.75]])

#### Réponse en amplitude 
- La réponse en fréquence H() est obtenue en évaluant la fonction de transfert à s = j:

- La réponse en amplitude est obtenue en prenant la valeur absolue de H(). 

- Chaque terme du dénominateur est la distance de j à l'emplacement d'un pôle, et chaque terme du numérateur est la distance de j à l'emplacement d'un zéro. La réponse en amplitude peut être obtenue en multipliant les distances de j à tous les zéros DZk et gain |K|, puis en le divisant par le produit des distances de j à tous les pôles DP k.
([[Chapitre-6.pdf#page=76&selection=0,20,43,1&color=yellow|Chapitre-6, p.76]])

> [!info] 
> $$H(j\omega) = \frac{N(j\omega)}{D(j\omega)}=|H(j\omega)|\angle H(j\omega
)$$

#### Réponse en phase 
- La réponse en phase est obtenue en prenant l'angle de H(). 
- Chaque terme du dénominateur est l'angle de j à l'emplacement d'un pôle, et chaque terme du numérateur est l'angle de j à l'emplacement d'un zéro. La réponse en phase peut être obtenue en ajoutant les angles de j à tous les zéros AZk et l’angle de K, K, puis en le soustrayant par la somme des angles de j à tous les pôles AP k. 
- À la fréquence  = ∞ 
	- chaque zéro contribue pour +90o à l’angle de phase H()
	- chaque pôle contribue pour –90o à l’angle de phase H()
([[Chapitre-6.pdf#page=77&selection=0,0,69,1&color=yellow|Chapitre-6, p.77]])

> [!tip] 
> Fonction de transfert revient a dire de trouver le rapport entre la sortie et l'entré:
> $$\frac{V_{o}}{V_{i}} = H(s) \qquad V_{o} = H(s) V_{in}$$

> [!question] Question examen
> ![[Chapitre-6.pdf#page=83&rect=28,36,573,809&color=yellow|Chapitre-6, p.83]]

> [!question] [[Chapitre-6.pdf#page=91&selection=105,0,110,67&color=yellow|Chapitre-6, p.91]]
> a) Tracer le circuit en représentant l’amplificateur opérationnel idéal par son modèle. 
> b) Tracer le même circuit mais cette fois-ci dans l’espace de Laplace.
> Nous devons trouver comment dessiner cela ....

#### Diagramme de Bode ? : Matlab (à voir)
??????

#### Filtre et Passe
