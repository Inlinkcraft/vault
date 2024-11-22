#GEL-1000 

Une source commandé est une source qui varie dépendant d'une autre variable présente dans le [[Circuit électrique|circuit]]. 

> [!Attention]
> Pour une source il est a notre avantage d'utilisé la [[Puissance électrique#Convention active|convention active]].

### Source commandé de tension
---
Une source commandé de [[Tension électrique|tension]] peut être controller selon une [[Tension électrique|tension]] ou [[Courant électrique|courant]] présent dans le circuit:

#### Commandé par une tension
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[S, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#TODO  Ajouter le symbole

$$V_{d} = \mu \ V_{c}$$
> $\mu$ est un gain sans dimensions

#### Commandé par un courant
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[S, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#TODO  Ajouter le symbole

$$V_{d} = R \ V_{c}$$
> $R$ est une [[Résistance électrique|résitance]] connue

### Source commandé de courant
---
Une source commandé de [[Courant électrique|courant]] peut être controller selon une [[Tension électrique|tension]] ou [[Courant électrique|courant]] présent dans le circuit:

#### Commandé par une tension
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[S, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#TODO  Ajouter le symbole

$$i_{d} = G \ V_{c}$$
> $G$ est une [[Conductance|conductance]] connue

#### Commandé par un courant
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[S, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document} 
```
#TODO  Ajouter le symbole

$$i_{d} = \alpha \ i_{c}$$
> $\alpha$ est un gain sans dimensions
