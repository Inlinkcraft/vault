---
name: Échelon unitaire
type: Matière
---
#GEL-1000 

L’échelon unitaire est utilisé pour modéliser un changement brusque d'une valeur à un instant donné.

### Definition
---
```tikz 
\begin{document} 
    \begin{tikzpicture}[domain=-1:1] 
        \draw[very thin,color=gray] (-1,-0.1) grid (1,1); 
        \draw[->] (-1,0) -- (1,0) node[right] {$t$}; 
        \draw[->] (0,-0.1) -- (0,1.1) node[above] {$f(x)$}; 
        \draw[color=red] (-1,0) -- (0, 0);
        \draw[color=red] (0,0) -- (0, 1);
        \draw[color=red] (0,1) -- (1, 1);
    \end{tikzpicture} 
\end{document} 
```
^graphique

$$u(t)=\begin{cases} 
0 & \text{pour } t < 0\\
1 & \text{pour } t \ge 0\\
\end{cases}$$
^equation