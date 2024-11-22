---
name: Condensateur électrique
type: Matière
---
#GEL-1000 

Objet ou [[Composante électrique|composante]] qui emmagasine l'énergie ou la restitue.
## Caractéristique du condensateur
---
#### Symbole:
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[C, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#### unité:
Farad: ($F$)
#### Capacité
La capacité d'un condensateur est décrite par l'équation suivante:
$$C=\frac{\epsilon A}{d}$$

## Modèle mathématique
---
L'équation qui décrit un condensateur et qui mets en relation le [[Courant électrique|courant]] et la [[Tension électrique|tension]].
$$i = C\frac{dv}{dt} \qquad \frac{V(s)}{I(s)} = \frac{1}{sC}$$
^GEL-1000-EQ

## Puissance en condensateur
---
La puissance d'un condensateur peut se calculer comme suit:
$$p = v \cdot i$$
^GEL-1000-EQ

## Travail en condensateur
---
Le travail d'un condensateur peut ce calculer comme suit:
$$w=\frac{1}{2}Cv^2$$
^GEL-1000-EQ

## Équivalent et diviseur
---
### Équivalent série
$$\frac{1}{C_{eqs}} = \sum_{k=1}^{n}\frac{1}{C_k}$$
### Diviseur de tension
$$V_{k}= \frac{C_{eqs}}{C_{k}}V_s$$
### Équivalent parallèle
$$C_{eqs} = \sum_{k=1}^{n}{C_k}$$
### Diviseur de courant
$$I_{k}= \frac{C_{k}}{C_{eqp}}I_{s}$$