---
name: Transformation de Laplace
type: Matière
---
#GEL-1000 
***
La transformée de Laplace est une méthode pour "simplifier" et résoudre une équations différentielles. La transformée de Laplace convertit les équations différentielles en équations algébriques en s ([[Chapitre-6.pdf#page=4&selection=54,29,55,46&color=yellow|p.4]]). 

### Introduction
---
Le concept de [[Phaseur|phaseur]] peut être généralisé en ajoutant une partie réelle $\sigma$ à la partie imaginaire $j\omega$, pour définir une variable complexe $s = \sigma + j\omega$. La transformation basée sur la variable complexe $s$ est appelée transformée de Laplace.
([[Chapitre-6.pdf#page=4&selection=4,0,19,8&color=yellow|p.4]])
### Notation
---
La paire de transformées de Laplace est représentée par: ([[Chapitre-6.pdf#page=4&selection=39,6,39,61&color=yellow|p.4]])
**Transformation de Laplace**
$$L[f(t)] = F(s)$$
**Transformation inverse de Laplace**
$$L^{-1}[F(s)] = f(t)$$
### Définition
---
La transformée de Laplace de f(t) est la transformée de Fourier de $f(t)e^{-\sigma t}$ ([[Chapitre-6.pdf#page=7&selection=216,0,223,1&color=yellow|p.7]]). soit:
$$L[f(t)]=\int_{0}^{\infty} f(t) e^{-st} dt$$
> [!tip] Preuve
> $$F(s)=F\left(\sigma+j\omega\right)=\int_{0^-}^{\infty}f(t)e^{-s t}d t=\int_{0^-}^{\infty}f(t)e^{-(\sigma+j\omega)t}d t=\int_{0^-}^{\infty}f(t)e^{-\sigma t}e^{-j\omega t}d t=F\left[f(t)e^{-\sigma t}\right]$$

### Tableau de transformation
---

|                **Fonction**                |         **$f(t)$**          |              **$F(s)$**               |
| :----------------------------------------: | :-------------------------: | :-----------------------------------: |
| [[Impulsion de Dirac\|Impulsion unitaire]] |         $\delta(t)$         |                  $1$                  |
|   [[Échelon unitaire\|Échelon unitaire]]   |           $u(t)$            |             $\frac{1}{s}$             |
|         [[Rampe\|Rampe unitaire]]          |           $r(t)$            |           $\frac{1}{s^{2}}$           |
| [[Fonction exponentielle\|Exponentielle]]  |        $e^{-at}u(t)$        |            $\frac{1}{s+a}$            |
|                   Sinus                    |    $\sin(\omega t)u(t)$     |   $\frac{\omega}{s^{2}+\omega^{2}}$   |
|                  Cosinus                   |    $\cos(\omega t)u(t)$     |     $\frac{s}{s^{2}+\omega^{2}}$      |
|               Rampe amortie                |       $te^{-at}u(t)$        |         $\frac{1}{(s+a)^{2}}$         |
|                Sinus amorti                | $e^{-at}\sin(\omega t)u(t)$ | $\frac{\omega}{(s+a)^{2}+\omega^{2}}$ |
|               Cosinus amorti               | $e^{-at}\cos(\omega t)u(t)$ |  $\frac{s+a}{(s+a)^{2}+\omega^{2}}$   |
### Propriété
---
#### Linéarité
###### Multiplication par une constante
La multiplication par une constante change rien:
$$L\left[ Kf(t)\right] = KF(s)$$
###### Addition
Une addition de plusieurs fonction peut devenir une transformation de ces terme:
$$L\left[ f_{1}(t) + f_{2}(t) + f_{3}(t) + \dots \right] = L\left[ f_{1}(t) \right] + L\left[ f_{2}(t) \right] + L\left[f_{3}(t)\right] + \dots  = F_{1}(s) + F_{2}(s) + F_{3}(s) + \dots$$

#### Dérivée
###### Dériver première
Transformation de la dérivée ([[Chapitre-6.pdf#page=12&selection=1,0,2,13&color=yellow|p.12]]):
$$L\left[ \frac{df(t)}{dt} \right] = sF(s)-f(0^-)$$
> [!Attention] Valeur initial
> $-f(0^-)$ est très important. Dans le cas le plus fréquent ce terme est d'une valeur de $0$. C'est-à-dire que pour faire la dériver dans le domaine des fréquence il suffit de multiplier $s$. Dans le cas inverse, soit que la valeur initial ne soit pas égale à $0$ cette valeur doit être présente. 

###### Dériver seconde
Transformation de la dérivée aux second ordre
$$L\left[ \frac{d^2f(t)}{dt^2} \right] = s^{2}F(s)-sf(0)-f'(0)$$

###### Dériver général
Transformation de la dérivée d'ordre $n$
$$L\left[ \frac{d^{n}f(t)}{dt^{n}} \right] = s^{n}F(s)-s^{n-1}f(0)-s^{n-2}f'(0)-s^{n-3}f''(0)-\dots-f^{n-1}(0)$$
#### Intégrale
Transformation de l'intégrale ([[Chapitre-6.pdf#page=12&selection=57,0,59,0&color=yellow|p.12]]):
$$L\left[ \int_{-\infty}^{t} f(t) \ dt \right] = \frac{1}{s}(F(s)+y(0))$$
> [!Attention] Valeur initial
> $y(0)$ est très important. Dans le cas le plus fréquent ce terme est d'une valeur de $0$. C'est-à-dire que pour faire l'intégrale dans le domaine des fréquence il suffit de multiplier $\frac{1}{s}$. Dans le cas inverse, soit que la valeur initial ne soit pas égale à $0$ cette valeur doit être présente. 

#### Translation

###### Translation l'axe du temps
Lorsqu'une translation survient dans le domaine du temps, une exponentielle sera ajouté au domaine des fréquence:
$$L[f(t-a)]=e^{-as}F(s)$$

###### Translation l'axe des fréquences
Lorsqu'une translation survient dans le domaine des fréquence, une exponentielle sera ajouté au domaine du temps:
$$L[e^{-at}f(t)]=F(s+a)$$
###### Changement d'échelle de temps
Le changement d'échelle de temps comme $at$ si $a > 0$:
$$L[f(at)]=\frac{1}{a}F\left( \frac{s}{a} \right)$$

#### Autre opération
Quelque autre opération courante:
###### Multiplier par $t$
$$L[tf(t)]=-\frac{dF(s)}{ds}$$
###### Multiplier par $t^{2}$
$$L[t^{2}f(t)]=\frac{d^{2}F(s)}{ds^{2}}$$
###### Multiplier par $t^n$
$$L[t^{n}f(t)]=(-1)^{n}\frac{d^{n}F(s)}{ds^{n}}$$
###### Diviser par $t$
$$L\left[ \frac{f(t)}{t} \right]= \int_{s}^{\infty}F(x) \ dx$$
#### Tableau récapitulatif

|          **Opération**           |              **$f(t)$**              |                                              **$F(s)$**                                               |
| :------------------------------: | :----------------------------------: | :---------------------------------------------------------------------------------------------------: |
|   Multiplier par une constante   |               $Kf(t)$                |                                                $KF(s)$                                                |
|             Addition             | $f_{1}(t)+f_{2}(t)+f_{3}(t) + \dots$ |                               $F_{1}(s) + F_{2}(s) + F_{3}(s) + \dots$                                |
|         Dérivée première         |           $\frac{df}{ft}$            |                                            $sF(s)-f(0^-)$                                             |
|         Dérivée seconde          |       $\frac{d^{2}f}{dt^{2}}$        |                                        $s^{2}F(s)-sf(0)-f'(0)$                                        |
|       Dérivée d'ordre $n$        |       $\frac{d^{n}f}{dt^{n}}$        | $\begin{array}{c} s^{n}F(s)-s^{n-1}f(0)-\\s^{n-2}f'(0)-s^{n-3}f''(0)-\dots-f^{n-1}(0)\end{array}$<br> |
|            Intégrale             |        $\int_{0}^{t} f(x) dx$        |                                       $\frac{1}{s}(F(s)+y(0))$                                        |
|        Décalage temporel         |               $f(t-a)$               |                                             $e^{-as}F(s)$                                             |
| Multiplier par une exponentielle |            $e^{-at}f(t)$             |                                               $F(s+a)$                                                |
|  Changement d'échelle de temps   |          $f(at), \quad a>0$          |                               $\frac{1}{a}F\left( \frac{s}{a} \right)$                                |
|        Multiplier par $t$        |               $tf(t)$                |                                          $-\frac{dF(s)}{ds}$                                          |
|       Multiplier par $t^2$       |             $t^{2}f(t)$              |                                      $\frac{d^{2}F(s)}{ds^{2}}$                                       |
|       Multiplier par $t^n$       |             $t^{n}f(t)$              |                                  $(-1)^{n}\frac{d^{n}F(s)}{ds^{n}}$                                   |
|         Diviser par $t$          |           $\frac{f(t)}{t}$           |                                     $\int_{s}^{\infty}F(x) \ dx$                                      |
