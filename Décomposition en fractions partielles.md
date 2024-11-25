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
- La décomposition en fractions partielles (DFP) consiste à exprimer un ==polynôme rationnel propre== comme une combinaison linéaire de ==polynômes rationnels propres de degrés plus petits==. 
- Après avoir représenté le ==polynôme rationnel propre== comme une somme de ==polynômes rationnels propres de plus petits degrés==, nous utilisons le [[Transformation de Laplace#Tableau de transformation|tableau en annexe]] pour trouver la transformée de Laplace inverse de chaque ==polynôme rationnel propre==. 
- La somme des transformations inverses est f(t).
([[Chapitre-6.pdf#page=25&selection=7,1,41,47&color=yellow|Chapitre-6, p.25]])

### Résolution
---
En générale, le quotient (dénominateur) aura la forme suivante:
$$Q_{s} = a_{n}(s-p_{1})(s-p_{2})(s-p_{3})\dots(s-p_{n})$$
> [!Note]
> Ici les $p_{1}, p_{2}, p_{3} \dots, p_{n}$ sont les pôle:
> - Réels simples
> - Complexes conjugés simples
> - Multiple
##### Cas 1 : pôles réel simples
1. Trouver la forme suivante: $$F(s)={\frac{P(s)}{Q(s)}}={\frac{K_{1}}{s-p_{1}}}+{\frac{K_{2}}{s-p_{2}}}+{\frac{K_{3}}{s-p_{3}}}+\ldots+{\frac{K_{n}}{s-p_{n}}}$$
2. Trouver les $K_{j}$ avec cette formule: $$K_{j}=\left.(s-p_{j})F(s)\right|_{s=p_{j}}$$
3. La réponse finale aura cette allure: $$f(t)=\left(K_{1}e^{p_{1}t}+K_{2}e^{p_{2}t}+...+K_{n}e^{p_{n}t}\right)u(t)$$
##### Cas 2 : pôles complexes simples
Si $p_{1}$ est un pôle complexe simple de $F(s)$, alors $p_{2} = p_{1}^{*}$ est aussi un pôle simple de $F(s)$.
([[Chapitre-6.pdf#page=28&selection=52,0,64,8&color=yellow|Chapitre-6, p.28]])
$$p_{1}=-a+jb \qquad p_{2} = -a-jb$$
1. Trouver l'expression de la forme $$F
   (s)= \frac{K_{1}}{(s-p_{1})}+\frac{K_{1}^{*}}{s-p_{1}^{*}} + \dots = \frac{A}{(s+a-jb)}+\frac{A^{*}}{(s+a+jb)}+\dots$$
  > [!Info] Annulation
  > Nous réduisons certaine fraction à zero pour trouver le coefficient des autre: 
  > ![[Chapitre-6.pdf#page=31&rect=252,94,367,660&color=yellow|Chapitre-6, p.31]]
1. Trouver A avec $$A=\left.(s-p_{1})F(s)\right|_{s=p_{1}}=\left.(s+a-jb)F(s)\right|_{s=-a+jb}$$
2. Finalement l'inverse sera donnée par: $$f(t) = |A|e^{j\angle A}e^{(-a+jb)t}+|A|e^{-j\angle A}e^{(-a-jb)t}=2|A|e^{-at}\cos{(bt+\angle A)}u(t)$$
##### Cas 3 : pôles multiples
Lorsque $s = p_{i}$ est une racine d'ordre $r$ de $Q(s)$ ([[Chapitre-6.pdf#page=37&selection=40,0,44,32&color=yellow|Chapitre-6, p.37]])
 1. Trouver la forme: $$F(s)=\frac{K_{i1}}{s-p_{i}}+\frac{K_{i2}}{\left(s-p_{i}\right)^{2}}+\ldots+\frac{K_{i j}}{\left(s-p_{i}\right)^{j}}+\ldots+\frac{K_{i r}}{\left(s-p_{i}\right)^{r}}+\dots$$
 2. Trouver les $K_{ij}$

##### Méthode des coefficient indéterminé
Transformation d'un polynôme rationnelle en prenant compte de sont degree: $F(s) =$
$$\frac{9s+5}{(s+4)(s^{2}+4s+20)} = \frac{A}{s+5}+\frac{Bs+C}{s_{2}2+4s+20}= \frac{(A+B)s^{2}+(4A+5B+C)s+20A+5C}{(s+5)(s^{2}2+4s+20)}$$
