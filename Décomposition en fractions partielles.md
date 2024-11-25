---
name: Décomposition en fractions partielles
type: Matière
---
#GEL-1000 
***
La décomposition en fractions partielles est une façons de calculer L'[[Transformation de Laplace inverse|inverse de la transformation Laplace]].

 > [!Tip] Insight
 > La [[Transformation de Laplace|transformée de Laplace]] $F(s)$ sous forme normalisée. 
 > $$F(s)=\!{\frac{N(s)}{D(s)}}\!=\!{\frac{b_{m}s^{m}+b_{m-1}s^{m-1}+b_{m-2}s^{m-2}+\dots+b_{1}s+b_{0}}{a_{n}s^{n}+a_{n-1}s^{n-1}+a_{n-2}s^{n-2}+\dots+a_{1}s+a_{0}}}\quad a_{n}\neq0$$
 > ([[Chapitre-6.pdf#page=25&selection=4,0,4,49&color=yellow|Chapitre-6, p.25]])

### Mise en place
---
Quelque charactéristique:
- $F(s)$ est appelé ==polynôme rationnel== car c'est le rapport de $N(s)$ à $D(s)$. Le degré du polynôme numérateur $N(s)$ est $m$, et le degré du polynôme dénominateur $D(s)$ est $n$. 
- Si $n > m$, $F(s)$ est appelé ==polynôme rationnel propre==. Si $m \ge n$, $F(s)$ est appelé ==polynôme rationnel impropre==. Si $m \ge n$, diviser $N(s)$ par $D(s)$ pour obtenir le quotient $Q(s)$ et le reste $R(s)$. $\frac{R(s)}{D(s)}$ est le polynôme rationnel propre.
- La décomposition en fractions partielles (DFP) consiste à exprimer un ==polynôme rationnel propre== comme une combinaison linéaire de polynômes rationnels propres de degrés plus petits.  Après avoir représenté le polynôme rationnel propre comme une somme de polynômes rationnels propres de plus petits degrés, nous utilisons le tableau en annexe pour trouver la transformée de Laplace inverse de chaque polynôme rationnel propre.  La somme des transformations inverses est f(t).
([[Chapitre-6.pdf#page=25&selection=7,1,41,47&color=yellow|Chapitre-6, p.25]])

##### Pôle simple
Si $F(s)$ a un pôle simple en $s = – a$, $D(s) = (s + a)D1(s)$. Le résidu à $s = – a$ est donné par
$$R = \left. (s+a) \frac{N(s)e^{st}}{(s+a)D_{1}(s)}\right|_{s=-a} \implies \frac{N(-a)e^{-at}}{D_{1}(-a)}$$
([[Chapitre-6.pdf#page=21&selection=18,0,19,21&color=yellow|Chapitre-6, p.21]])
##### Pôle multiple
Si $F(s)$ a $r$ pôles à $s = – a$, $D(s) = (s + a)^{r} D1(s)$. Le résidu à $s = – a$ est donné par
$$R = \frac{1}{(r-1)!} \frac{d^{r-1}}{ds^{r-1}} \left. \left[ (s+a)^{r} \frac{N(s)e^{st}}{(s+a)^{r}D_{1}(s)} \right] \right|_{s=-a} \implies \frac{1}{(r-1)!} \frac{d^{r-1}}{ds^{r-1}} \left. \left[\frac{N(s)e^{st}}{D_{1}(s)} \right] \right|_{s=-a} $$
([[Chapitre-6.pdf#page=21&selection=23,0,30,13&color=yellow|Chapitre-6, p.21]])

##### Pôle complexe
Les pôle complexe ce traite comme les pôle simple ou multiple a l'exeption qu'il ne faut pas oublier le conjuguer du nombre complexe.

> [!Tip]
> Les nombre complexe peuvent mener à des fonction sinusoïdale
### Procédure de résolution
---
Procédure de transformation de Laplace inverse : 
1. Multipliyer le numérateur par $e^{st}$: $F(s) e^{st} = \frac{N(s)e^{st}}{D(s)}$
2. Factoriser $D(s)$ le dénominateur
3. Trouver les residus (Formule ci-haut)
4. Prendre la somme des residus
([[Chapitre-6.pdf#page=21&selection=34,0,56,32&color=yellow|Chapitre-6, p.21]])
