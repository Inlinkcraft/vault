---
name: Calcule par conditionnement
type: Matière
---
#STT-2920 

Le calcule par conditionnement est une façons d'optenir la probabilité d'un [[Événement|événement]] en sachant la probabilité d'un autre [[Événement|événement]] ainsi que ces intersection en utilisant la [[Lois des probabilité total|lois des probabilité total]]

### Modèle mathématique
---
Supposons que 
- $A$ est un événement dont on cherche la probabilité 
- $X$ est une variable aléatoire discrète de loi connue
- L’on connaît $\mathbb{P}[A|X = x]$ pour chaque $x \in S_X$ .
Par la [[Lois des probabilité total|loi des probabilité total]], on a alors:
$$\mathbb{P}[A] = \sum_{x\in S_X}\mathbb{P}[A|X=x]\mathbb{P}[X = x] = \sum_{x\in S_X}\mathbb{P}[A|X=x]p_{X}(x)$$