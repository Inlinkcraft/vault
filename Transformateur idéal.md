---
name: Transformateur idéal
type: Matière
---
#GEL-1000 

Le transformateur idéal est une [[Composante électrique|composante électronique]] complexe qui permet de modifier la [[Tension électrique|tension]] et le [[Courant électrique|courant]] dans un [[Circuit électrique|circuit]].

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}[american]
\draw (0,0) to[I, l=$I$, v=$V$] (3,0); 
\end{circuitikz} 
\end{document}
```

#TODO  Ajouter le symbole

> [!Info]
> Tous les borne ayant le point aurons la même polarité.
> De plus, si le courant entre par le point il sortira par le point.

### Définition mathématique
---
La definition d'un transformateur idéal est par le ratio du nombre de tours pour chacune des bobine.
$$\frac{V_{2}(t)}{V_{1}(t)} = \frac{N_{2}}{N_{1}} \qquad \frac{i_{2}(t)}{i_{1}(t)} = -\frac{N_{1}}{N_{2}}$$

> [!Info] Ratio du transformateur ($a$)
> Le ratio du transformateur $a$ est une valeur qui est décrite comme suit:
> $$a = \frac{N_{2}}{N_{1}} \qquad \frac{1}{a} = \frac{N_{1}}{N_{2}}$$
