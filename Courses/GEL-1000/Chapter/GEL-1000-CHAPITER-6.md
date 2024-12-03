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

Manipulation de circuit à domaine de Laplace
---
![[Manipulation de circuit à domaine de Laplace]]

Méthode d'analyse par la transformation de Laplace
---
![[Méthode d'analyse par la transformation de Laplace]]

Fonction de transfert 
---
![[Fonction de transfert]]



#### Filtre et Passe


La convolution
---

### Definition mathématique
---
**Symbole**: $*$
$$\begin{array}{rcl}
H(s) \times X(s) & \leftrightarrow & h(t) * x(t) \\
Y(s) & \leftrightarrow & y(t)
\end{array}$$

![[Chapitre-6.pdf#page=101&rect=289,85,536,759|Chapitre-6, p.101]]

##### Propriété
 Commutativité f 1(t)  f 2(t) = f 2(t)  f 1(t) 
 Associativité [f 1(t)  f 2(t)]  f 3(t) = f 1(t)  [f 2(t)  f 3(t)]
 Distributivité f 1(t)  [f 2(t) + f3(t)] = f1(t)  f 2(t) + f 1(t)  f 3(t) 
 Décalage temporal If f(t) = f 1(t)  f 2(t), then f 1(t – t d)  f 2(t) = f(t – t d) 
 Propriété de Convolution de la transformée de Laplace L[f 1(t)  f 2(t)] = F1(s)F2(s)
([[Chapitre-6.pdf#page=102&selection=2,0,150,3&color=yellow|Chapitre-6, p.102]])

> [!example] 
> ![[Chapitre-6.pdf#page=103&rect=42,78,564,781&color=yellow|Chapitre-6, p.103]]
> ![[Chapitre-6.pdf#page=104&rect=44,73,557,787&color=yellow|Chapitre-6, p.104]]

### Convolutions impliquant la fonction delta de Dirac
---
De la propriété de tamisage de la fonction delta de Dirac, on obtient ([[Chapitre-6.pdf#page=106&selection=4,0,5,7&color=yellow|Chapitre-6, p.106]])
$$\delta (t) * f(t) = \int^{t}_{-\infty} \delta (\lambda)f(t - \lambda) \ d \lambda = f(t)$$![[Chapitre-6.pdf#page=107&rect=247,514,519,773&color=yellow|Chapitre-6, p.107]]
Diagramme de Bode ? : Matlab (à voir)
---
Le diagramme de Bode représente la réponse d’amplitude en dB (décibels) et la réponse de phase d’un système décrit par la fonction de transfert H(s).
([[Chapitre-6.pdf#page=110&selection=4,0,5,71&color=yellow|Chapitre-6, p.110]])
La réponse d’amplitude en dB est définie comme suit : M dB() = 20 log 10(|H()|)
([[Chapitre-6.pdf#page=110&selection=13,0,24,3&color=yellow|Chapitre-6, p.110]])
`logspace(0.1, N)`

**Convertion en décibel**
$$M_{dB}(\omega) = 20 \log_{10}(|H(\omega)|)$$

Révision
---
![[Chapitre-6.pdf#page=115&rect=37,28,571,781&color=yellow|Chapitre-6, p.115]]![[Chapitre-6.pdf#page=116&rect=50,33,565,785&color=yellow|Chapitre-6, p.116]]![[Chapitre-6.pdf#page=120&rect=29,91,520,752&color=yellow|Chapitre-6, p.120]]

> [!example] 
> ![[Chapitre-6.pdf#page=98&rect=108,98,346,673&color=yellow|Chapitre-6, p.98]]
> ```circuitjs
> $ 64 0.000005 1.0312258501325766 50 5 50 5e-11
> r 480 192 608 192 0 50
> r 608 192 608 304 0 100
> v 480 304 480 192 0 0 40 120 0 0 0.5
> w 480 304 608 304 0
> w 608 304 672 304 0
> w 672 304 672 192 1
> w 672 192 608 192 0
> ```
> ```circuitjs
> ```
> $$\begin{array}{lll}
  & = &  \\
\end{array}$$
