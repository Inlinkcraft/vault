---
name: Inductance électrique
type: Matière
---
#GEL-1000 

Objet ou [[Composante électrique|composante]] s'oppose au changement de courant.

## Caractéristique de l'inductance
---
#### Symbole:
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[L, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#### unité:
Henri: ($H$)
#### Inductance
L'inductance d'un condensateur est décrite par l'équation suivante:
$$L=\frac{\mu N^{2}A}{h} \qquad N \varphi = L\, i$$

### Représentation Laplace
---
La représentation d'une inductance dans le domaine de [[Transformation de Laplace|Laplace]]
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[european]
\draw (0,0) to[R, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
Formule:

| [[Impédance]] | [[Admittance]] |
| :-----------: | :------------: |
|     $Ls$      | $\frac{1}{Ls}$ |

## Lois de Faraday
---
L'équation qui décrit une inductance et qui mets en relation le [[Courant électrique|courant]] et la [[Tension électrique|tension]].
$$v = L\frac{di}{dt}$$
^GEL-1000-EQ

## Puissance en inductance
---
La puissance d'un inductance peut se calculer comme suit:
$$p = v \cdot i$$
^GEL-1000-EQ

## Travail en inductance
---
Le travail d'un inductance peut ce calculer comme suit:
$$w=\frac{1}{2}L \, i^2$$
^GEL-1000-EQ

## Équivalent et diviseur
---
### Équivalent série
$$L_{eqs} = \sum_{k = 0}^{n}L_{k}$$
### Diviseur de tension
$$V_{k}= \frac{L_{k}}{L_{eqs}}V_s$$
### Équivalent parallèle
$$\frac{1}{L_{eqp}} = \sum_{k = 0}^{n}\frac{1}{L_{k}}$$
### Diviseur de courant
$$I_{k}= \frac{L_{eqp}}{L_{k}}I_s$$