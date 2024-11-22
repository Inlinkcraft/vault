---
name: Impulsion de Dirac
type: Matière
---
#GEL-1000 

La fonction exponentielle est présente dans plusieurs domaine des mathématique et physique.

### Definition
---
```tikz 
\begin{document} 
    \begin{tikzpicture}[domain=0:1] 
        \draw[very thin,color=gray] (-1,-0.1) grid (1,1); 
        \draw[->] (-1,0) -- (1,0) node[right] {$t$}; 
        \draw[->] (0,-0.1) -- (0,1.1) node[above] {$f(x)$}; 
        \draw[color=red] (-1,0) -- (0, 0);
        \draw[color=red] plot (\x,{exp(-3*\x)});
    \end{tikzpicture} 
\end{document} 
```
^graphique

$$f(t) = Ae^{-\alpha t} \qquad (u(t))$$
^equation