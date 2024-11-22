---
name: Porte
type: Matière
---
#GEL-1000 

La porte sert de fonction d’activation à durée limitée. Elle est composé de deux ou plus [[Échelon unitaire|échelon unitaire]]

### Definition
---
```tikz 
\begin{document} 
    \begin{tikzpicture}[domain=-1:1] 
        \draw[very thin,color=gray] (-1,-0.1) grid (1,1); 
        \draw[->] (-1,0) -- (1,0) node[right] {$t$}; 
        \draw[->] (0,-0.1) -- (0,1.1) node[above] {$f(x)$}; 
        \draw[color=red] (-1,0) -- (-0.5, 0);
        \draw[color=red] (-0.5,0) -- (-0.5, 1);
        \draw[color=red] (-0.5,1) -- (0.5, 1);
        \draw[color=red] (0.5,1) -- (0.5, 0);
        \draw[color=red] (0.5,0) -- (1, 0);
    \end{tikzpicture} 
\end{document} 
```
^graphique

$$\Pi(t) = u(t+0.5) - u(t-0.5) \qquad \Pi(t)=\begin{cases} 
1 & \text{pour } -0.5 \le t \le 0.5\\
0 & \text{sinon}
\end{cases}$$
^equation