---
name: Impulsion de Dirac
type: Matière
---
#GEL-1000 

L’impulsion de Dirac est la dériver de l'[[Échelon unitaire|échelon unitaire]]. Elle permet de prendre une mesurer a $t=0$

### Definition
---
```tikz 
\begin{document} 
    \begin{tikzpicture}[domain=-1:1] 
        \draw[very thin,color=gray] (-1,-0.1) grid (1,1); 
        \draw[->] (-1,0) -- (1,0) node[right] {$t$}; 
        \draw[->] (0,-0.1) -- (0,1.1) node[above] {$f(x)$}; 
        \draw[color=red] (-1,0) -- (1, 0);
        \draw[color=red, ->] (0,0) -- (0, 1);
    \end{tikzpicture} 
\end{document} 
```
^graphique

$$\delta(t) = \frac{d}{dt}[u(t)] \qquad \delta(t)=\begin{cases} 
1 & \text{pour } t = 0\\
0 & \text{sinon}\\
\end{cases}$$
^equation