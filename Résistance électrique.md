---
name: Résistance électrique
type: Matière
---
#GEL-1000 

Objet ou [[Composante électrique|composante]] qui oppose le déplacement des électron, **aka** la [[Résistivité|résistivité]].

## Caractéristique de la résistance
---
#### Symbole:
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[R, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#### unité:
Ohm: ($\ohm$)

## Lois d'ohm
---
La loi d'ohm permet de mettre en relation la résistance électrique, le [[Courant électrique|courant]] et la [[Tension électrique|tension]].
$$v=Ri \qquad i=Gv \qquad \text{où} \qquad G = \frac{1}{R} \qquad R = \frac{1}{G}$$
^GEL-1000-EQ

>[!Info]
>Lorsque le comportement de la résistance n'est pas linéaire celle-ci se nomme une [[Varistance électrique|varistance]].

## Puissance en resistance
---
La puissance d'une résistance peut se calculer comme suit:
$$p = v \cdot i \qquad p = \frac{v^{2}}{R} \qquad p = Ri^2$$
^GEL-1000-EQ

## Travail en resistance
---
Le travail d'une resistance peut ce calculer comme suit:
$$w=\int_{-\infty}^{t}p \ dt$$
^GEL-1000-EQ

## Équivalent et diviseur
---
### Équivalent série
$$R_{eqs} = R_{1} + R_{2} + \dots + R_{n}$$
### Diviseur de tension
$$V_{k}= \frac{R_{k}}{R_{eqs}}V_s$$
### Équivalent parallèle
$$\frac{1}{R_{eqp}} = \frac{1}{R_{1}} + \frac{1}{R_{2}} + \dots + \frac{1}{R_{n}}$$
### Diviseur de courant
$$I_{k}= \frac{R_{eqp}}{R_{k}}I_s$$