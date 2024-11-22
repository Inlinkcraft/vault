---
name: Notation asymptotique
type: Matière
---
#GLO-2100

La notation asymptotique est un regroupement de famille de fonction représentant la tendance du temps d'execution d'un [[Algorithme|algorithme]] plus le nombre d'élément a traiter augmente.

### Notation Big-Ho $O(n)$
---
$O(n)$ représente la borne supérieur qui ne sera jamais franchie par $f(n)$ quel-contes à une constante près. $n_0$ représente la valeur de $n$ où $O(n)$ est toujours supérieur $f(n)$ 

> [!Info]
> Par définition:
> $$O(1) \subset O(\log(n)) \subset O(n) \subset O(n \log(n)) \subset O(n²) \subset O(2^{n}) \subset O(10^{n}) \subset O(n!)$$
> La règle du maximum découle de cet formule ces-à-dire que le si plusieurs [[Algorithme|algorithmes]] sont exécuté l'un a la suite de l'autre lui qui aura le plus gros $O(n)$ "mangera" les autre. 

#### Le pire cas $C_{\text{worst}}$
le pire cas est le concept qui estime que les donné sont tous placer dans le pire ordre d'execution possible.

### Notation Omega $\Omega(n)$
---
$\Omega(n)$ représente la borne inférieur qui ne sera jamais franchie par $f(n)$ quel-contes à une constante près. $n_0$ représente la valeur de $n$ où $\Omega(n)$ est toujours inférieur $f(n)$ 

### Notation Theta $\Theta(n)$
---
$\Theta(n)$ représente la borne inférieur et supérieur qui ne sera jamais franchie par $f(n)$ quel-contes à une constante près. $n_0$ représente la valeur de $n$ où $\Omega(n)$ est toujours inférieur et supérieur $f(n)$ 
