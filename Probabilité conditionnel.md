---
name: Probabilité conditionnel
type: Matière
---
#STT-2920

Lorsqu'une information supplémentaire est donnée dans une [[Expérience aléatoire|expérience aléatoire]] cela peut changer la probabilité que cet événement produise.

### Représentation mathématique
---
Pour noter l'événement $A$ sachant $B$ il suffit d'écrire:
$$\mathbb{P}[A|B] = \frac{\mathbb{P}[A \cap B]}{\mathbb{P}[B]}$$

Dans un cas équiprobable:
$$\mathbb{P}[A|B] = \frac{|A \cap B|}{|B|}$$

> [!info]
> Si $B$ influence la probabilité alors $A$ dépend de $B$
> Si $B$ influence pas la probabilité de $A$ alors A est indépendant.

### Propriété
---
> [!info] Ce sont les [[Axiom de Kolmogorov|axiom de Kolmogorov]] transposé

Si $\mathbb{P}[B] > 0$, alors on a:
- $0 \le \mathbb{P}[A|V] \le 1$ Pour tout $A \subset \Omega$
- $\mathbb{P}[\emptyset|B] = 0$ et $\mathbb{P}[\Omega|B]=1$
- Si $A_{1}, A_{2}, A_{3}, \dots, A_{n}\subset \Omega$ sont mutuellement exclusifs, on a :
    - $\mathbb{P}[A_{1} \cup A_{2} \cup A_{3} \cup \dots \cup A_{n}|B] = \sum_{i=1}^{n}\mathbb{P}[A_{i}|B]$
    - $\mathbb{P}[(\cup_{n=1}^{\infty}A_{n})|B] = \sum_{i=1}^{\infty}\mathbb{P}[A_{i}|B]$

> [!Attention]
> La probabilité conditionnel n'est pas commutative
> $$\mathbb{P}[A|B] \ne \mathbb{P}[B|A]$$

#### Règle de multiplication
La règle de multiplication est une propriété de la probabilité conditionnelle qui est basé sur sa définition et qui est très utilisé:
$$\mathbb{P}[A \cap B] = \mathbb{P}[B]\mathbb{P}[A|B]$$
$$\mathbb{P}[A \cap B] = \mathbb{P}[A]\mathbb{P}[B|A]$$
$$\mathbb{P}[A_{1} \cap A_{2} \cap A_{3}] = \mathbb{P}[A_1]\mathbb{P}[A_{2} \cap A{3}|A_{1}]= \mathbb{P}[A_{1}]\mathbb{P}[A_{2}|A_{1}]\mathbb{P}[A_{3}|A_{1} \cap A_{2}]$$

>[!Info] Notation
>$$\mathbb{P}[B_{1} \cap B_{2} \cap B_{3}] = \mathbb{P}[B_{1}, B_{2}, B_{3}] = \mathbb{P}[B_{1}B_{2}B_{3}] = \mathbb{P}[BBB]$$
