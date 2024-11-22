---
name: Amplificateur opérationnel
type: Matière
---
#GEL-1000 

L'amplificateur opérationnel permet d'amplifier ou d'effectuer certain calcul mathématique avec les variable présente dans le [[Circuit électrique|circuit]].

### Procédure d'analyse
---
- [i] La rétroaction négative est importante, car sans celle-ci l'amplis-op saturera.
- [i] Utilisation des [[Lois de Kirchhoff|lois de Kirchhoff (Adition des courant)]]
- [i] Validation de la linéarité suite à la résolution
- [i] La tension à borne d'entré d'inversion est 0 

#### Ampli-op commun
- [[Amplificateur inverseur]]
- [[Amplificateur non-inverseur]]
- [[Amplificateur de sommation]]
- [[Amplificateur différence]]
- [[Amplificateur en cascade]]
- [[Amplificateur dérivateur]]
- [[Amplificateur intégrateur]]

### Comportement
---
Le comportement d'un amplificateur opérationnel est décris dans ce graphique:

```tikz 
\begin{document} 
\begin{tikzpicture}[domain=-2:2] 
\draw[very thin,color=gray] (-2,-2) grid (2,2); 
\draw[->] (-2,0) -- (2,0) node[right] {$x$}; 
\draw[->] (0,-2) -- (0,2) node[above] {$V(x)$}; 
\draw[color=red, domain=-2:-1] plot (\x,-1) node[left] {$-Vcc$}; 
\draw[color=red, domain=-1:1] plot (\x,\x); 
\draw[color=red, domain=1:2] plot (\x,1) node[right] {$Vcc$}; 
\end{tikzpicture} 
\end{document} 
```

- $V_o$ ne peut pas excédé $V_{cc}$. On dit alors que l'amplificateur est saturé positivement
- $V_o$ ne peut pas être inférieur à $-V_{cc}$. On dit alors que l'amplificateur est saturé négativement
- Le but dans l'utilisation d'un amplificateur opérationnel ces de rester dans la zone linéaire à l'aide d'une rétroaction négative.

#TODO Ajouter le symbole

> [!Attention]
> Un amplificateur opérationnel idéal aurait les valeur suivante
> - $A_{ol} = \infty$
> - $R_{d} = \infty$
> - $R_{o} = 0$
> 
> Due a cela certaine propriété en découle soit:
> - $V_{1} = V_{2}$
> - La [[Source commandé|source]] se comporte comme une [[Source commandé|source]] idéal.

