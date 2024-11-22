---
name: Axiom de kolmogorov
type: Matière
---
#STT-2920

Axiome définie pour travaillé avec des probabilité 

### Axiom
---
1. Pour tout $A \subset \Omega$, on a $O \le \mathbb{P}[A] \le 1$
2. $\mathbb{P}[\emptyset] = 0$ et $\mathbb{P}[\Omega] = 1$
3. Si on a $A_{1}, A_{2}, \dots, A_{n} \subset \Omega$ qui sont [[STT-2920-CLASS-1#Vers une approche uniform|mutuellement exclusif]] alors:
$$\mathbb{P}[A_{1}\cup A_{2}\cup \dots \cup A_{n}] = \sum_{i=1}^{n}\mathbb{P}[A_i]$$

### Conséquence des axiom
---
#### 1. Cas équiprobable (fini)
Un retour au [[Cas discret|cas discret]] soit:
$$\mathbb{P}[A] = \frac{|A|}{|\Omega|}$$

#### 2. Complémentarité
"L'inverse":
$$\mathbb{P}[A] = 1 - \mathbb{P}[A^c]$$

#### 3. Identité du Poincaré (inclusion-exclusion)
1. $\mathbb{P}[A \cup B] = \mathbb{P}[A] + \mathbb{P}[B] - \mathbb{P}[A \cap B]$
2. $\mathbb{P}[A \cup B \cup C] = \mathbb{P}[A] + \mathbb{P}[B] + \mathbb{P}[C] - \mathbb{P}[A \cap B] - \mathbb{P}[A \cap C] - \mathbb{P}[B \cap C] + \mathbb{P}[A \cap B \cap C]$
3. $\mathbb{P}[E_{1} \cup \dots \cup E_{n}] = \sum_{j=1}^{n}(-1)^{j+1} \sum_{1<i_{1}<\dots<i_{j}\le n}\mathbb{P}[E_{i_{1}}\cap \dots \cap E_{i_j}]$

#### 4. Monotonicité
Inclusion (Implication):
$$A \subset B \longrightarrow \mathbb{P}[A] \le \mathbb{P}[B]$$