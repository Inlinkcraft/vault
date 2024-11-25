---
name: Transformation de Laplace inverse
type: Matière
---
#GEL-1000 
***
L'inverse de la [[Transformation de Laplace|transformation de Laplace]].


### Définition mathématique
---
$$f(t) = L^{-1}[F(s)] = \frac{1}{2\pi j}\int_{\sigma-j \infty}^{\sigma+\infty}F(s)e^{st} \ ds$$
> Cette intégrale peut être évaluée à l'aide du [[Théorème du résidus|théorème du résidu]]
> ([[Chapitre-6.pdf#page=20&selection=146,0,148,21&color=yellow|Chapitre-6, p.20]])

### Méthode de résolution possible
---
- [[Transformation de Laplace#Tableau de transformation|Utilisation d'un tableau]]
- [[Théorème du résidus]]
- [[Décomposition en fractions partielles]]