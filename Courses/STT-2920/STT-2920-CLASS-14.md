---
name: Cours-14
type: Class
course: STT-2920
date: 2024-10-23T15:30
Complete: true
---
#school/STT-2920 
***

# Matière abordée

- [[Loi de Bernoulli|Rappel processus de Bernouilli]]
- [[Loi binomiale|Rappel loi binomial]]
- [[Loi géométrique|Rappel loi géométrique]]
- [[Loi géométrique#Propriété de perte de mémoire|Propriété de perte de mémoire de la loi géométrique]]
- [[Loi exponentielle#Un processus limite de la loi géométrique|Loi exponentielle, un processus limite de la loi géométrique]]
- [[Loi de Poisson#Comme la limite d’une loi binomiale|Loi de Poisson comme la limite d’une loi binomiale]]

### Propriété de perte de mémoire de la loi exponentielle 
---
Soit T ∼ exponentielle(λ). Soient t, s ∈ R+, alors P [T > t + s|T > s] = P [T > t] 
Démonstration : P [T > t] = Z ∞ t λe−λudu = e−λt P [T > t + s|T > s] = P [T > t + s ∩ T > s] P [T > s] = P [T > t + s] P [T > s] = e−λ(t+s) e−λs = e−λt On a donc P [T > t + s|T > s] = P [T > t] = e−λt Interprétation : Dans un processus de Poisson, si on a déjà écoulé s secondes sans succès (observation), la probabilité d’écoulé t secondes supplémentaires sans succès est la même que la probabilité d’écoulé t secondes sans succès depuis le début du processus. 
Remarque : Lorsqu’une v.a. respecte (2), on dit qu’elle possède la propriété de perte de mémoire. La loi exponentielle est la seule loi continue possédant la propriété de perte de mémoire. 
[[STT-2920-Chapter-7.pdf#page=10&selection=0,53,262,1&color=yellow|STT-2920-Chapter-7, p.10]]

---

Le processus de Poisson Un processus de Poisson peut être vue comme l’analogue du processus de Bernoulli, mais dans un système temporelle continue. Typiquement, on s’intéresse à des observations qui surviennent de telle sorte que le nombre d’observations dans une unité de temps suit une loi de Poisson de paramètre λ observations par unité de temps. On a alors que le temps entre les observations suit la loi exponentielle de paramètre λ (On a donc en moyenne 1 λ unités de temps par observation, c’est le temps moyen entre 2 observations). Voici un schéma illustrant un processus de Poisson. Temps • • • T1 T2 T3 N : Nombre d’observations dans un intervalle de temps Souvent, on note N(t) la variable aléatoire donnant le nombre d’observations durant les t premières unités de temps. On a donc que N(t) ∼ Poisson(λt). De la même façon, si 0 < s < t, on note [N(t) − N(s)] la variable aléatoire dénotant le nombre d’observations entre les instants t et s. Puisque cet intervalle de temps est de durée t − s, on a que [N(t) − N(s)] ∼ Poisson(λ(t − s)). On note souvent Ti le temps entre l’observation no i − 1 et l’observation no i. On a que tous les Ti sont i.i.d selon la loi exponentielle(λ).
([[STT-2920-Chapter-7.pdf#page=11&selection=0,0,176,1&color=yellow|STT-2920-Chapter-7, p.11]])
### Le processus de Poisson

Un processus de Poisson décrit un nombre d’observations suivant une loi de Poisson dans un temps continu. Si $N(t)$ est le nombre d’observations durant les $t$ premières unités de temps, alors $N(t) \sim \text{Poisson}(\lambda t)$.

#### Exemple
Un serveur reçoit des requêtes selon un processus de Poisson d’intensité 6 requêtes/heure.

1. Probabilité de 15 requêtes en 3 heures ?
2. Probabilité d’attendre au moins 30 minutes pour la prochaine requête ?
3. Espérance et variance du temps entre 2 requêtes successives ?

---

### La fonction Gamma

Pour $\alpha > 0$, la fonction Gamma est définie par:
$$
\Gamma(\alpha) = \int_0^{\infty} u^{\alpha - 1} e^{-u} \, du
$$

---

### La loi gamma

Pour $\alpha > 0$ et $\lambda > 0$, la loi gamma est définie par :
$$
f(x) = \frac{\lambda^\alpha}{\Gamma(\alpha)} x^{\alpha - 1} e^{-\lambda x}
$$

---

### Conséquences et Théorèmes

1. **Somme de variables exponentielles**  
   Si $X_i \sim \text{exponentielle}(\lambda)$, alors $\sum_{i=1}^n X_i \sim \text{gamma}(n, \lambda)$.

---

### Exemple d’application

Un appareil utilise une composante électronique avec une durée de vie exponentielle moyenne de 100 heures. Au cours de 2 semaines, on peut s'attendre à utiliser environ 3,36 composantes.

1. Combien de copies sont nécessaires pour 90% de probabilité de fonctionnement sans interruption ?
2. Utilisation de la loi de gamma pour déterminer le temps de fonctionnement attendu.

