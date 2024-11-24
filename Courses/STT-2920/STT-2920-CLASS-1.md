---
name: Cours-1
type: Class
course: STT-2920
date: 2024-09-04T15:30
status: "Compléter"
---
#school/STT-2920 
***
# Plan de cours
- Dépannage sont à la deuxième heure du cours du lundi (sauf dans certain cas)
- Centre d'aide pour les exercise est accessible avec une priorité pour les statistique

## Contenue du cours
- Les note de cours des année antérieur
- Note de cours par chapitre avec les exercise
- Les notes de cours version longue

## Examen
- Feuille de note 8½x11 permise à l'examen
- Doit avoir 50% aux examen en plus qu'a la session pour réussir

# Chapitre 1: Introduction à la théorie de la probabilité
## Terminologie
- [[Expérience aléatoire]]
- [[Ensemble fondamental]]
- [[Événement]]
- En compréhension: Description de l'ensemble en mots
- En extension: Liste exhaustive de l'ensemble.
- Cardinal: d'un ensemble est le nombre d'élément de l'ensemble obtenue avec $|X|$

## Forme possible de l'ensemble fondamental

![[Ensemble fondamental#Forme]]

## Probabilité

![[Événement#Probabilité]]

Dans le cas ou tous les événements sont équiprobable une simplification peut être fait soit la suivante:
$$\mathbb{P}[A] = \frac{|A|}{|\Omega|}$$

> [!Rappel]
> Rappel sur les série géométrique
> $$\sum_{n=0}^{\infty}ar^{n}=\frac{a}{1-r}\qquad \text{si} \ |r|<1 \ \text{sinon la série diverge}$$
> $$\sum_{n=0}^{m}r^{n} = \frac{1-r^{m+1}}{1-r}$$
> $$\sum_{n=0}^{\infty}r^{n} = \frac{1}{1-r} \qquad \text{si} \ |r|<1$$
> $$\sum_{n=1}^{\infty}nr^{n} = \frac{r}{(1-r)^2} \qquad \text{si} \ |r|<1$$
> $$\sum_{n=1}^{\infty}n^2r^{n} = \frac{r(r+1)}{(1-r)^3} \qquad \text{si} \ |r|<1$$
> [[Série géométrique|voir plus]]

### Cas discret
Dans tous les cas ou l'[[Ensemble fondamental|ensemble fondamental]] est dénombrable la méthode du [[Cas discret|cas discret]] est utilisable.

### Cas continue
Dans le cas ou l'[[Ensemble fondamental|ensemble fondamental]] est n'est pas dénombrable, mais continue et uniforme il est possible de procédé avec un rapport de longueur ou d'air soit le [[Cas continue|cas continue]].

## Vers une approche uniform

> [!Rappel]
> Rappel sur les ensemble
> - $A \cup B$ : l'ensemble des $\omega$ dans A et/ou B:  **Union/Disjonction**
> - $A \cap B$ : l'ensemble des $\omega$ dans A et B: **Intersection/Conjonction**
> - $A \backslash B$ : l'ensemble des $\omega$ dans A, mais pas dans B: **Différence**
> - $A^{c}:=A\backslash\Omega$ : l'ensemble des $\omega$ qui sont pas dans A: **Complément**
> - $A \tiny\Delta \small B$ : l'ensemble des $\omega$ dans A ou bien dans B:  **Ou exclusif/Différence symétrique**
> - Deux élément sont incompatible ou disjoin si $A \cap B = \emptyset$: **Mutuellement exclusif**
> [[Ensemble|voir plus]]