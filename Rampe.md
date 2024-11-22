---
name: Rampe
type: Matière
---
#GEL-1000 

La rampe est l'intégrale de l'[[Échelon unitaire|échelon unitaire]]

### Definition
---Rampe
```tikz 
\begin{document} 
    \begin{tikzpicture}[domain=-1:1] 
        \draw[very thin,color=gray] (-1,-0.1) grid (1,1); 
        \draw[->] (-1,0) -- (1,0) node[right] {$t$}; 
        \draw[->] (0,-0.1) -- (0,1.1) node[above] {$f(x)$}; 
        \draw[color=red] (-1,0) -- (0, 0);
        \draw[color=red] plot (0,0) -- (1, 1);
    \end{tikzpicture} 
\end{document} 
```
^graphique

Impulsion de Dirac$$r(t) = \int_{-\infty}^{t}u(t) \ dt \qquad r(t)=\begin{cases} 
0 & \text{pour } t < 0\\
t & \text{pour } t \ge 0\\
\end{cases}$$
^equation