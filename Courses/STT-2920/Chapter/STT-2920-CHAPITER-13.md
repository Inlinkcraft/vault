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
> > **Distribution d'échantillonage à utiliser:**
> > 	population mère normale avec $\sigma$ connue, $\sigma = 0.25$V
> > 	$$z=\frac{\bar{X}-\mu}{\frac{\sigma}{\sqrt{ n }}} \sim N(0, 1)$$
> > 	sous $H_{0}$
> > 	$$Z = \frac{\bar{X}-12.5}{\frac{\sigma}{\sqrt{ n }}} \sim N(0, 1)$$
> > 	![[STT-2920-Chapter-13.pdf#page=5&rect=183,41,284,114&color=yellow|STT-2920-Chapter-13, p.5]]
> > 	$\frac{\alpha}{2}=0.025$
> > **Règle de décision**
> > 	$z_{\frac{\alpha}{2}} = 1.96$
> > 	règle:
> > 		rejet de $H_{0}: |Z_{\text{obs}}| > 1.96$
> > **Valeur observée**
> > 	$Z_{\text{obs}} = \frac{\bar{X}-12.5}{\frac{\sigma}{\sqrt{ n }}} = \frac{12.53-12.5}{\frac{0.25}{\sqrt{ 100 }}}=1.2$
> > 	$|Z_{\text{obs}}| = 1.2 \ngtr 1.96$, on ne rejette pas $H_{0}$
> > **Conclusion:**
> > Au seuil de signification 5%, aucune évidence statistique ne nous permet de croire que le nouveau procédé change le voltage moyen théorique
> 
([[STT-2920-Chapter-13.pdf#page=7&selection=0,0,37,2&color=yellow|STT-2920-Chapter-13, p.7]])

##### Le seuil de signification empirique (la valeur p ou p-value)
 le plus petit seuil de signification possible faisant en sorte que le test mène au rejet de $H_{0}$ (i.e. à la validation de $H_{1}$)
([[STT-2920-Chapter-13.pdf#page=10&selection=20,49,30,1&color=yellow|STT-2920-Chapter-13, p.10]])

 $\mathbb{P} [|Z| > |Z_{\text{obs}}| |H_{0} \text{ vraie}]$ dans un test bilatéral 
 $\mathbb{P} [Z < Z_{\text{obs}} |H_{0} \text{ vraie}]$  dans un test unilatéral à gauche 
 $\mathbb{P} [Z > Z_{\text{obs}} |H_{0} \text{ vraie}]$ dans un test unilatéral à droite
([[STT-2920-Chapter-13.pdf#page=10&selection=45,0,102,32&color=red|STT-2920-Chapter-13, p.10]])

> [!example] 
> on avait $Z_{obs}=1.2$ donc
> $$p_value = \mathbb{P}[|Z| > |Z_{obs}|] = \mathbb{P}[|Z| > 1.2] = 2\mathbb{P}[|Z| > 1.2]$$
> $$= 2(1-\mathbb{P}[|Z| < 1.2]) = 2(1-\Phi(1.2)) = 2(1-0.8849) = \dots = 0.2302$$
> **Remarque**: $p_value > \alpha = 0.05$, c'est pour cela que l'on n'avait pas rejeter $H_{0}$
> 

Rappel des distributions d’échantillonnage
![[STT-2920-Chapter-13.pdf#page=12&rect=18,14,442,172&color=red|STT-2920-Chapter-13, p.12]]

>[!example] 
>>[!question] 
>>![[STT-2920-Chapter-13.pdf#page=13&rect=37,160,439,217&color=red|STT-2920-Chapter-13, p.13]]
>
>>[!success] Solution
>><u>**Solution**</u>
>> Soit μ la réelle durée de vie moyenne des pneus avec le nouveau procédé.
>> <u>**Hypothèses**</u>
>> $$H_{0} : \mu = 30000 \qquad H_{1} : \mu > 30000$$
>> On a donc un test unilatéral à droite au seuil $\alpha = 5\%$
>> <u>**Collecte des données échantillonnale**</u>
>> On a $n = 16$, $\bar{x} = 32000$km et $s = 3500$km
>> <u>**Distribution d'échantillonnage à utiliser**</u>
>> Puisque que l'on a une population mère normale et $\sigma$ est inconnu, on a que
>> $$T = \frac{\bar{x}-\mu_{0}}{\frac{S}{\sqrt{ n }}} \sim t_{n-1}$$
>> Sous $H_{0}$: on a que $\frac{\bar{x}-30000}{\frac{S}{\sqrt{ n }}} \sim t_{n-1}$
>> <u>**Règle de décision**</u>
>> La valeur critique est $t_{15;0.05} = 1.753$.
>> Règle de décision : Rejet de $H_{0}$ si $T > 1.753$, non rejet de $H_{0}$ sinon.
>> <u>**Valeur observée de décision**</u>
>> Valeur observée : $T_{obs} = \frac{\bar{x}-\mu_{0}}{\frac{S}{\sqrt{ n }}} = \frac{32000-30000}{\frac{3500}{\sqrt{ 16 }}} = 2.29$
>> Décision: Puisque $T_{obs} = 2.29 > 1.753$, on rejette $H_0$ et on valide donc $H_{1}$
>> <u>**Conclusion**</u>
>> Au seuil de signification 5%, on a une évidence statistique permettant de croire que le nouveau procédé améliore la durée de vie moyenne des pneus
>> <u>**Estimation de la p-value**</u>
>> p-value = $\mathbb{P}[T > T_{obs}] = \mathbb{P}[T_{15} > 2.29] = ?$
>> Tout ce que l’on peut dire avec la table de la loi de Student est que la p-value est entre 0.010 et 0.025.
>> 

> [!example] 
> > [!question] 
> > ![[STT-2920-Chapter-13.pdf#page=15&rect=35,171,437,216|STT-2920-Chapter-13, p.15]]
> 
> > [!success] solution
> > ![[STT-2920-Chapter-13.pdf#page=15&rect=22,40,404,155|STT-2920-Chapter-13, p.15]]
> > ![[STT-2920-Chapter-13.pdf#page=16&rect=23,196,327,229|STT-2920-Chapter-13, p.16]]
> > Sous $H_{0}$:
> > $$\chi^{2}= \frac{(n-1)s^{2}}{(0.10)^{2}} \sim \chi_{n-1}^{2}$$
> > ![[STT-2920-Chapter-13.pdf#page=16&rect=24,3,431,160|STT-2920-Chapter-13, p.16]]

> [!example] 
> > [!question] 
> > ![[STT-2920-Chapter-13.pdf#page=17&rect=35,140,437,221|STT-2920-Chapter-13, p.17]]
> 
> >[!success] solution
> >![[STT-2920-Chapter-13.pdf#page=17&rect=23,0,269,133|STT-2920-Chapter-13, p.17]]
> >![[STT-2920-Chapter-13.pdf#page=18&rect=25,181,413,231|STT-2920-Chapter-13, p.18]]
> >...
> >![[STT-2920-Chapter-13.pdf#page=18&rect=27,2,363,133|STT-2920-Chapter-13, p.18]]
> >![[STT-2920-Chapter-13.pdf#page=19&rect=25,115,416,233|STT-2920-Chapter-13, p.19]]

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