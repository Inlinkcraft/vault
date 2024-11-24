---
name: Cours-11
type: Class
course: GEL-1000
date: 2024-10-15T08:30
status: "Compléter"
---
#school/GEL-1000  
*** 

# Chapitre 4: Fonction d'excitation

Début des [[Excitation électrique|Fonction d'excitation]] et retour  rapide sur la [[Principe de superposition|superposition]]

# Chapitre 4: Fonctions d'excitation

## Objectifs

- Reconnaître les excitations électriques périodiques
- Comprendre le comportement des fonctions d’excitation simples comme l’échelon, l’impulsion et la rampe ainsi que leurs relations
- Savoir décomposer les excitations électriques apériodiques en fonctions d’excitations simples
- Comprendre le rôle des paramètres des fonctions exponentielles complexes
- Comprendre ce qu’est un phaseur
- Retrouver la fonction réelle à partir d’une fonction exponentielle complexe
- Savoir que tout signal périodique peut se décomposer en une somme de signaux sinusoïdaux
- Comprendre la base de la transformation de Fourier
- Reconnaître les composantes d’un spectre, dont la fondamentale et les harmoniques

---

## Plan du cours

- Excitations électriques
- Fonctions apériodiques
- Fonctions exponentielles
- Fonctions sinusoïdales
- Fonctions périodiques
- Analyse de Fourier

---

## Excitations électriques

### Excitations apériodiques
Les excitations apériodiques sont des signaux qui ne se répètent pas régulièrement dans le temps.

### Excitations périodiques
Les excitations périodiques se répètent à intervalles réguliers. Exemples :
- Carré symétrique
- Carré positif
- Sinusoïdal alternatif
- Redressé simple alternance
- Redressé double alternance

---

## Décomposition de signaux complexes en signaux simples - Principe de superposition

Le principe de superposition permet de décomposer une excitation complexe en une somme d’excitations simples, que l’on peut traiter individuellement. La réponse à l’excitation complexe est la somme des réponses aux excitations individuelles.

---

## Fonctions apériodiques

### L'échelon unitaire (fonction de Heaviside)
L’échelon unitaire est utilisé pour modéliser une excitation qui change brusquement de valeur à un instant donné.

### La porte Π(t)
La fonction porte est définie par deux échelons et sert de fonction d’activation à durée limitée.

### La rampe unitaire r(t)
La rampe unitaire est définie comme l’intégrale de l’échelon unitaire. C'est une droite de pente 1, qui commence à $ t = 0 $.

### L’impulsion unitaire δ(t)
L’impulsion de Dirac est la dérivée de l’échelon unitaire et a une surface égale à 1.

---

## Nombres complexes et phaseurs

Les nombres complexes sont une représentation puissante pour les sinusoïdes. Un nombre complexe \( z \) peut être écrit sous forme rectangulaire \( z = x + jy \) ou sous forme polaire \( z = re^{j\phi} \). 

---

### Phaseurs
Les phaseurs permettent de représenter une sinusoïde comme la composante réelle d’un vecteur dans le plan complexe. La transformation entre le domaine temporel et le domaine des phaseurs est donnée par : 

\[
v(t) = V_m \cos(\omega t + \phi) \Rightarrow V = V_m \angle \phi
\]

## Transformation sinusoïdale-phaseur

La transformation entre sinusoïdes et phaseurs peut être résumée par les identités suivantes :

- \(\sin(\omega t \pm 180^\circ) = -\sin(\omega t)\)
- \(\cos(\omega t \pm 180^\circ) = -\cos(\omega t)\)
- \(\sin(\omega t \pm 90^\circ) = \pm \cos(\omega t)\)
- \(\cos(\omega t \pm 90^\circ) = \mp \sin(\omega t)\)

En appliquant une dérivée ou une intégrale à un phaseur, on obtient les transformations suivantes :
- **Dérivée** : \( \frac{d v(t)}{dt} \rightarrow j\omega V \)
- **Intégrale** : \( \int v(t) \, dt \rightarrow \frac{V}{j\omega} \)

---

## Fonctions exponentielles

### Fonctions exponentielles réelles
Les fonctions exponentielles réelles peuvent être croissantes, décroissantes ou constantes, selon le signe de \(\sigma\) :
- **Croissante** : \(\sigma > 0\)
- **Décroissante** : \(\sigma < 0\)
- **Constante** : \(\sigma = 0\)

### Fonctions exponentielles complexes
Une fonction exponentielle complexe peut être écrite comme : 
\[ x(t) = X e^{st} \]
où \( s = \sigma + j\omega \) est la fréquence complexe, et \( X e^{j\phi} \) est le phaseur (amplitude complexe).

---

## Série de Fourier

### Introduction
Joseph Fourier a découvert que toute fonction périodique non sinusoïdale peut être représentée comme une somme infinie de fonctions sinusoïdales. Une fonction périodique satisfait : 
\[ f(t) = f(t + nT) \]
où \( n \) est un entier et \( T \) est la période.

### Série trigonométrique de Fourier
La série de Fourier permet de représenter une fonction périodique \( f(t) \) en termes de fonctions sinus et cosinus :
\[ f(t) = a_0 + \sum_{n=1}^{\infty} (a_n \cos(n \omega_0 t) + b_n \sin(n \omega_0 t)) \]
où \( \omega_0 = \frac{2 \pi}{T} \) est la fréquence fondamentale en radians par seconde.

### Coefficients de Fourier
Les coefficients de Fourier \( a_n \) et \( b_n \) sont donnés par :
- \( a_0 = \frac{1}{T} \int_0^T f(t) \, dt \)
- \( a_n = \frac{2}{T} \int_0^T f(t) \cos(n \omega_0 t) \, dt \)
- \( b_n = \frac{2}{T} \int_0^T f(t) \sin(n \omega_0 t) \, dt \)

### Harmoniques
Les termes \( \sin(n \omega_0 t) \) et \( \cos(n \omega_0 t) \) sont appelés les harmoniques de la fonction \( f(t) \), où \( n \) représente l'ordre de l'harmonique.

---

## Propriétés de symétrie

### Symétrie paire et impaire
- **Fonction paire** : \( f(t) = f(-t) \) — les coefficients \( b_n = 0 \)
- **Fonction impaire** : \( f(t) = -f(-t) \) — les coefficients \( a_n = 0 \)

### Symétrie demi-onde
Une fonction ayant une symétrie demi-onde satisfait : 
\[ f\left(t + \frac{T}{2}\right) = -f(t) \]
Les fonctions avec symétrie demi-onde contiennent uniquement des harmoniques impaires.

---

## Forme amplitude-phase de Fourier

La série de Fourier peut être exprimée sous une forme amplitude-phase alternative :
\[ f(t) = a_0 + \sum_{n=1}^{\infty} A_n \cos(n \omega_0 t + \phi_n) \]
où \( A_n \) et \( \phi_n \) sont l’amplitude et la phase, respectivement, définis par :
- \( A_n = \sqrt{a_n^2 + b_n^2} \)
- \( \phi_n = \arctan\left(\frac{b_n}{a_n}\right) \)

---

## Applications de la transformation de Fourier dans les circuits

L'analyse de Fourier est particulièrement utile pour analyser les circuits excités par des signaux non sinusoïdaux :
1. Exprimer l'excitation comme une série de Fourier.
2. Transformer le circuit dans le domaine fréquentiel.
3. Trouver les réponses des composants DC et AC de la série de Fourier.
4. Combiner les réponses en utilisant le principe de superposition.

---

## Puissance moyenne et valeur RMS

Pour une excitation périodique dans un circuit, la puissance moyenne totale est la somme des puissances moyennes de chaque composante harmonique. La puissance moyenne \( P \) est donnée par :
\[ P = \frac{1}{2} V_{\text{dc}} I_{\text{dc}} + \sum_{n=1}^{\infty} \frac{1}{2} V_n I_n \cos(\theta_n - \phi_n) \]
La valeur RMS de la fonction périodique \( f(t) \) est :
\[ f_{\text{rms}} = \sqrt{a_0^2 + \frac{1}{2} \sum_{n=1}^{\infty} (a_n^2 + b_n^2)} \]

---

## Synthèse de Fourier

La synthèse de Fourier consiste à recombiner les termes d'une série trigonométrique pour reconstituer la forme d'onde originale. Par exemple, pour un signal en dents de scie, on peut utiliser les composantes continue, fondamentale, et les harmoniques pour recréer le signal.

---

## Références supplémentaires

- **Circuits électriques** par Hoang Le-Huy, Les Presses de l'Université Laval, 2004.
- **Introduction to Electric Circuits** par Dorf R.C., Svoboda J.A., Wiley, 2004.
- **The Analysis and Design of Linear Circuits** par Thomas R.E., Rosa A.J., Wiley, 2004.

---

