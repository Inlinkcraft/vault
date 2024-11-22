---
name: Source indépendante
type: Matière
---
#GEL-1000 

Une source indépendante est une source qui peut varier dans le temps mais celle-ci ne dépendra jamais d'un autre variable présente dans le [[Circuit électrique|circuit]]. 

> [!Attention]
> Pour une source il est a notre avantage d'utilisé la [[Puissance électrique#Convention active|convention active]].

### Source de tension indépendante
---
Une source de [[Tension électrique|tension]] indépendante ressemble à:

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[S, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#TODO  Ajouter le symbole

$$V(t) = f(t)$$

### Source de courant indépendante
---
Une source de [[Courant électrique|courant]] indépendante ressemble à:

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[S, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#TODO  Ajouter le symbole

$$I(t) = g(t)$$