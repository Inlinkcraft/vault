---name: Cours-21
type: Class
course: GEL-1000
date: 2024-11-29T09:30
status: À Réviser
---
#school/GEL-1000  
*** 
# Avant le cour
## Plan de cours
- Réponse d'un circuit ? / Dépassement / Décomposition ?

## Todo
- 

---
# Matière abordée

- 

## Notes supplémentaire

> [!example] 
> ![[Chapitre-6.pdf#page=125&rect=108,61,549,763|Chapitre-6, p.125]]
> 

> Une unité manquante  $\to$ -1 point

|                                                      |                                                                                                                                                                                                                      |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Delai de réponse (Delay time) t d                    | Temps requis pour atteindre 50% de la valeur finale                                                                                                                                                                  |
| Temps de montée (Rise time) tr                       | Temps requis par un système sous-amorti, pour atteindre son premier cycle d’oscillation. Si le système est sur-amorti, alors le temps de montée est défini comme le temps de montée de 10% à 90% de sa valeur finale |
| Temps de crête (Peak time) tp                        | Temps requis pour atteindre la première crête, i.e. l’amplitude maximale de la première oscillation, ou 1 er dépassement                                                                                             |
| Dépassement maximale (Maximum overshoot) M p         | Différence entre le dépassement maximale et la valeur finale (en %)                                                                                                                                                  |
| Temps d’établissement (Settling time) t s            | Temps requis pour atteindre le régime permanent (spécifié entre 2 et 5%)                                                                                                                                             |
| Erreur de régime permanent (Steady-State error) e ss | Écart entre la réponse et la valeur finale au temps infini                                                                                                                                                           |
([[Chapitre-6.pdf#page=124&selection=6,0,40,57&color=yellow|Chapitre-6, p.124]])

> [!example] 
> ![[Chapitre-6.pdf#page=98&rect=104,90,581,774&color=yellow|Chapitre-6, p.98]]
> L' inductance ce comporte comme un cours-circuits
> $$i_{L}(0^-)=\frac{120}{50}A = 2.4A$$
> $$i_{L}(t) = 2.4u(t) = 2.4(1-u(t))A$$
> $$V_{L}(0^-)=120V$$
> $$V_{l}(t)=120(1-u(t))V$$
> ----
> $$i_{1}(0^-)=0$$
> Ramener les chose dans Laplace
> $$\underbrace{250}_{R} \qquad \underbrace{\frac{1}{0.12 \times 10^{-3}s}}_{C} \qquad \underbrace{0.05s}_{L}$$
> Courant circulatoires
> $$0.05s(j_{1} + j_{2}) + 250 (j_{1} - j_{2}) = 0$$
> $$250(j_{2} - j_{1}) + \frac{j_{2}}{0.12 \times 10^{-3}s}$$
> $$\begin{bmatrix} 0.05s+250 & -250 \\ -250 & 250 + \frac{1}{0.12 \times 10 ^{-3}s} \end{bmatrix}\begin{bmatrix} j_{1} \\ j_{2} \end{bmatrix} = \begin{bmatrix} -0.05s i_{g} \\ 0 \end{bmatrix}$$
> $$\frac{\left|\begin{array}{cc} -0.05s i_{g} & -250 \\ 0 & 250 + \frac{1}{0.12 \times 10 ^{-3}s} \end{array}\right|}{\left|\begin{array}{cc} 0.05s+250 & -250 \\ -250 & 250 + \frac{1}{0.12 \times 10 ^{-3}s} \end{array}\right|}$$
> $$\frac{-0.5s i_{g} \left( 250 + \frac{1}{0.12 \times 10 ^{-3}s} \right)}{(10.255+250)\left( 250+\frac{1}{0.12 \times 10^{-3}s}-\frac{250 \times 250}{62500} \right)}$$
> ...
> $$\frac{-0.05(250s \times 0.12 \times 10^{-3} + 1) i_{g}}{0.12 \times 10 ^{-3} \times 250 \times 0.05s + 0.05 + 250}$$
> ...
> $$i_{1} = -\frac{(a_{2}s^{2} + a_{0}s)i_{g}}{b_{2}s^{2} + b_{1}s + b_{0}}$$
> $$i_{g} = 2.5u(t)$$
> $$i_{1}(b_{2}s^{2}+b_{1}s+b_{0}) = (a_{1}s + a_{0})i_{g}$$
> $$b_{2} \frac{d^{2}i_{1}}{dt^{2}} + b_{1} \frac{di_{1}}{dt} + b_{0} = a_{2} \frac{d^{2}i_{g}}{dt^{2}} + a_{1} \frac{di_{g}}{dt}$$
> ...
> $$\cases{b_{2} \frac{d^{2}x}{dt^{2}} + b_{1} \frac{dx}{dt} + b_{0}x = 0 \\ b_{2} \frac{d^{2}x}{dt^{2}} + b_{1} \frac{dx}{dt} + b_{0}x = 1}$$
> $$x = x_{H}+x_{P} \qquad X_{H} = A_{1}e^{s_{1}t}+A_{2}e^{s_{2}t}$$
> $$\cases{A_{1} = -\frac{s_{2}}{s_{2}-s_{1}}x_{p} \\ A_{2} = \frac{s_{1}}{s_{2} - s_{1}}x_{p}}$$
> $$b_{2}s^{2} + b_{1}s_{1} + b_{0} = c?$$

---
# En retrospective