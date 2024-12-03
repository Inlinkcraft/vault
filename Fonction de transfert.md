---
name: Fonction de transfert
type: Matière
---
#GEL-1000 
***
Dans le circuit transformé de Laplace avec des ==conditions initiales nulles==, le rapport de la sortie dans le domaine s à l'entrée dans le domaine s est défini comme la fonction de transfert. ([[Chapitre-6.pdf#page=70&selection=3,1,6,31&color=yellow|Chapitre-6, p.70]])

![[Chapitre-6.pdf#page=71&rect=432,169,569,641&color=yellow|Chapitre-6, p.71]]
### Définition mathématique
---
Soit $X(s)$ la représentation du domaine $s$ de l'entrée, et soit $Y(s)$ la représentation du domaine $s$ de la sortie. La fonction de transfert est alors:
$$H(s) = \frac{Y(s)}{X(s)}$$
$$Y(s) = H(s){X(s)}$$
([[Chapitre-6.pdf#page=70&selection=10,1,11,77&color=yellow|Chapitre-6, p.70]])
> [!note] $H(s)$
> $H(s)$ est "ADN" du système
> Se nomme la "Fonction réseau"

$$H(s) = K \frac{(s-z_{1})(s-z_{2})\dots(s-z_{m})}{(s-p_{1})(s-p_{2})}$$
> [!note] 
> où p1, p2, ….., pn sont des pôles, z 1, z 2, ….., zm sont des zéros, et K est une constante.
> ([[Chapitre-6.pdf#page=75&selection=21,0,40,14&color=yellow|Chapitre-6, p.75]])
### Fonction de réseau
---
![[Chapitre-6.pdf#page=72&rect=324,80,557,778&color=yellow|Chapitre-6, p.72]]

| Fonction de réseau    |                         | $H(s)$                                    |
| --------------------- | ----------------------- | ----------------------------------------- |
| Immitance             | Impédance               | $Z_1(s)=\frac{V_{1}(s)}{I_{1}(s)}$        |
|                       | Admittance              | $Y_1(s)=\frac{I_{1}(s)}{V_{1}(s)}$        |
| Fonction de transfert | Impédance de transfert  | $Z_{12}(s)=\frac{V_{2}(s)}{I_{1}(s)}$     |
|                       | Admittance de transfert | $Y_{12}(s)=\frac{I_{2}(s)}{V_{1}(s)}$     |
|                       | Gain en tension         | $A_{V_{12}}(s)=\frac{V_{2}(s)}{V_{1}(s)}$ |
|                       | Gain en courant         | $A_{i_{12}}(s)=\frac{I_{2}(s)}{I_{1}(s)}$ |

##### Réponse à l’impulsion, réponse à l’échelon, réponse à la rampe
La sortie $y(t)$ est obtenue en prenant la transformée de Laplace inverse de $Y(s)$, c'est-à-dire: $$y(t) = L-1[Y(s)] = L-1[H(s)X(s)]$$**Réponse impulsionnelle**: $$x(t) = \delta(t) \qquad X(s) = 1 \qquad Y(s) = H(s) \times 1 = H(s) \qquad h(t) = L^{-1}[H(s)]$$**Réponse à l'échelon:** $$x(t) = u(t) \qquad X(s) = \frac{1}{s} \qquad Y(s) = \frac{H(s)}{s} \qquad h_{s}(t) = L^{-1}\left[ \frac{H(s)}{s} \right]$$
**Réponse à la rampe:** $$x(t) = tu(t) \qquad X(s) = \frac{1}{s^{2}} \qquad Y(s) = \frac{H(s)}{s^{2}} \qquad h_{r}(t) = L^{-1}\left[ \frac{H(s)}{s^{2}} \right]$$
([[Chapitre-6.pdf#page=74&selection=12,0,70,1&color=yellow|Chapitre-6, p.74]])

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
