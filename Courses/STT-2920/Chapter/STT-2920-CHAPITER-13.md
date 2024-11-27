---
name: Tests d'hypothèse
type: Chapter
course: STT-2920
---

Test d’hypothèse (Présentation)
---
- l’hypothèse $H0$ nommée l’hypothèse nulle et l’hypothèse 
- $H1$ nommée la contre-hypothèse (ou hypothèse alternative)
([[STT-2920-Chapter-13.pdf#page=3&selection=6,0,17,53&color=yellow|STT-2920-Chapter-13, p.3]])

- Dans ce chapitre, nous nous attarderons aux tests d’hypothèse paramétriques, i.e. dont les hypothèses portent sur un paramètre
([[STT-2920-Chapter-13.pdf#page=3&selection=21,0,22,35&color=yellow|STT-2920-Chapter-13, p.3]])

- L’hypothèse $H0$ est l’hypothèse qui est acceptée jusqu’à présent, par norme établie ou étude précédente. Elle sera de la forme $H0 : θ = θ_{0}$. Cette hypothèse est est considérée vraie jusqu’à preuve du contraire dans la mécannique du test.
([[STT-2920-Chapter-13.pdf#page=3&selection=28,0,50,47&color=yellow|STT-2920-Chapter-13, p.3]])

- L’hypothèse H1 suggère une modification possible de θ. Cette hypothèse peut être de une des 3 formes suivantes : 
$$\underbrace{H_{1} : \theta < \theta_{0}}_{\text{test unilatéral à gauche}} \qquad \underbrace{H_{1} : \theta \ne \theta_{0}}_{\text{test bilatéral}} \qquad \underbrace{H_{1} : \theta > \theta_{0}}_{\text{test unilatéral à droite}}$$
([[STT-2920-Chapter-13.pdf#page=3&selection=54,0,98,24&color=yellow|STT-2920-Chapter-13, p.3]])

> [!info] Bref
> Dans un test d’hypothèse, on se sert d’un échantillon aléatoire (plus précisément d’une statistique de l’échantillon) pour arriver à une des deux décisions suivantes : (on rejette H0 i.e. on confirme l’hypothèse H1) ou bien (on ne rejette pas l’hypothèse H0, i.e. on ne peut pas confirmer l’hypothèse H1)
([[STT-2920-Chapter-13.pdf#page=3&selection=99,0,117,1&color=yellow|STT-2920-Chapter-13, p.3]])

> [!question] 
> Dans le cas des tests d’hypothèse sur la moyenne μ d’une population, 
> l’hypothèse $H0$ sera de la forme $H0 : μ = μ_{0}$ 
> l’hypothèse $H1$ peut être d’une des 3 formes : 
> $H1 : μ < μ_{0}$ ou bien $H1 : μ \ne μ_{0}$ ou bien $H1 : μ > μ_{0}$. <Pour prendre la décision, on construira une règle de décision qui s’appuiera sur la statistique $\bar{X}$, ou plus précisément sur la satistique $ $ et sur le fait que  ∼ N(0, 1) sous l’hypothèse H0
([[STT-2920-Chapter-13.pdf#page=4&selection=8,0,121,1&color=yellow|STT-2920-Chapter-13, p.4]])

Le seuil de signification et la zone de rejet
([[STT-2920-Chapter-13.pdf#page=5&selection=6,0,6,44&color=yellow|STT-2920-Chapter-13, p.5]])
α est la probabilité de rejeter H0 si H0 est vraie, c’est-à-dire de rejeter à tort H0
$$\alpha = \mathbb{P}[\text{Rejeter } H_{0} | H_{0} \text{ est vrai}]$$
![[STT-2920-Chapter-13.pdf#page=5&rect=50,36,403,115&color=yellow|STT-2920-Chapter-13, p.5]]
**Règle de décision**:
![[STT-2920-Chapter-13.pdf#page=6&rect=24,156,203,205&color=yellow|STT-2920-Chapter-13, p.6]]

$$Z_{\text{obs}} = \frac{\bar{X}-\mu_{0}}{\frac{\sigma}{\sqrt{n}}}$$
> [!example] Example
> > [!question] Question
> > Une industrie produit des piles. Un ingénieur propose des modifications au processus de fabrication dans le but d’augmenter la durée de vie des piles produites. Toutefois, il ne faudrait pas que ces modifications affectent le voltage moyen des piles produites. ==Avec le procédé actuel==, on sait ==que le voltage des piles suit une loi normale de moyenne 12.5 V==, avec ==un écart-type 0.25 V==. Avant de faire les modifications à grande échelle, il faudrait vérifier qu’effectivement le voltage moyen n’est pas affecté. On supposera ici que la distribution ==du voltage des piles produites avec le nouveau procédé est normale avec même écart-type qu’avant==. On ==produit un échantillon de 100 piles avec le nouveau procédé== et on ==obtient un voltage moyen de 12, 53 V.== Faites un ==test d’hypothèse au seuil de signification α = 0.05== permettant de ==vérifier si le voltage moyen du nouveau procédé diffère de 12.5 V==.
> 
> > [!success] Réponse
> > Soit $u$ : :e réelle coltage moyen du nouveau procédé
> > Hypothèse:
> > 	$H_{0}: \mu = 12.5$V (le nouveau procédé ne change pas le voltage moyen)
> > 	$H_{1}: \mu \ne 12.5$V
> > on a un test bilatéeal au seuil $\alpha = 0.05$
> > Collecte des donnée échantillonnales: $n = 100, \ \ \bar{x} = 12.53$V
> > Distribution d'échantillonage à utiliser:
> > 	population mère normale avec $\sigma$ connue, $\sigma = 0.25$V
> > 	$$z=\frac{\bar{X}-\mu}{\frac{\sigma}{\sqrt{ n }}} \sim N(0, 1)$$
> > 	sous $H_{0}$
> > 	$$Z = \frac{\bar{X}-12.5}{\frac{\sigma}{\sqrt{ n }}} \sim N(0, 1)$$
> > 	![[STT-2920-Chapter-13.pdf#page=5&rect=183,41,284,114&color=yellow|STT-2920-Chapter-13, p.5]]
> > 	$\frac{\alpha}{2}=0.025$
> > Règle de décision
> > 	$z_{\frac{\alpha}{2}} = 1.96$
> > 	règle:
> > 		rejet de $H_{0}: |Z_{\text{obs}}| > 1.96$
> > Valeur observée
> > 	$Z_{\text{obs}} = \frac{\bar{X}-12.5}{\frac{\sigma}{\sqrt{ n }}} = \frac{12.53-12.5}{\frac{0.25}{\sqrt{ n }}} $
> 
([[STT-2920-Chapter-13.pdf#page=7&selection=0,0,37,2&color=yellow|STT-2920-Chapter-13, p.7]])

Test d’hypothèse sur une moyenne (présentation détaillée)
---
Test d’hypothèse sur une moyenne (un premier exemple)
---
Le seuil de signification empirique (la valeur p ou p-value)
---
Rappel des distributions d’échantillonnage
---
Exemple d’un test d’hypothèse sur un écart-type (une variance)
---
Exemple d’un test d’hypothèse sur la comparaison de deux moyennes
---
Les types d’erreur et fonction puissance
---
Principe de dualité entre un test bilatéral et un intervalle de confiance
---