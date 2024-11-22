---
name: Coefficient binomial
type: Matière
---
#STT-2920

Les coefficient binomial sont utiliser dans plusieurs facette des mathématique
$${n \choose k} = \frac{n!}{k!(n-k)!}$$

### Propriété
---
#### symétrie
$${n \choose k} = {n \choose n - k}$$

#### Sommation d'une ligne
$$2^{n}= \sum_{k=0}^{n}{n \choose k}$$

>[!Info]
>Cette propriété est équivalente a faire la somation d'une ligne du [[Triangle de Pascale|triangle de Pascale]]

#### Formule d'addition
$${n \choose k} = {n-1 \choose k} + {n-1 \choose k - 1}$$

>[!Info]
>Cette propriété est équivalente a faire la somation des deux élément de la ligne précédente du [[Triangle de Pascale|triangle de Pascale]]

#### Autre Propriété
$${n+m \choose k} = \sum_{j=0}^{k}{n \choose j}{m \choose k-j}$$
$${2n \choose n} = \sum_{j=0}^{n}{n \choose j}^2$$

### Coefficient multinomial
---
Le coefficient multinomial est une variation du coefficient binomial. Celui-ci permet de séparé totalement tous les élément parmi un nombre x d'urne.
$${n \choose k_{1}, k_{2}, \dots, k_{n}} = \frac{n!}{k_{1}! k_{2}!\dots k_{n}!}$$