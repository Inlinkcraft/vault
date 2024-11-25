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


##### Cas 3 : pôles multiples
