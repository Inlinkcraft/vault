---
name: Fonction de transfert
type: Matière
---
#GEL-1000 
***
Dans le circuit transformé de Laplace avec des ==conditions initiales nulles==, le rapport de la sortie dans le domaine s à l'entrée dans le domaine s est défini comme la fonction de transfert. ([[Chapitre-6.pdf#page=70&selection=3,1,6,31&color=yellow|Chapitre-6, p.70]])

### Définition mathématique
---
Soit $X(s)$ la représentation du domaine $s$ de l'entrée, et soit $Y(s)$ la représentation du domaine $s$ de la sortie. La fonction de transfert est alors:
$$$$
([[Chapitre-6.pdf#page=70&selection=10,1,11,77&color=yellow|Chapitre-6, p.70]])



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
