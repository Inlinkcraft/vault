---
name: Intervalles de confiance
type: Chapter
course: STT-2920
---
.....
.....
.....
Intervalles de confiance:
$\sigma^{2}$ au niveau de confiance $1-a$  est de la forme
([[STT-2920-Chapter-11-12.pdf#page=23&selection=10,0,21,15&color=yellow|STT-2920-Chapter-11-12, p.23]])

### Exemple
170.05, 170.01, 170.09, 170.11, 169.95, 170.03, 170.05, 170.00, 170.06
([[STT-2920-Chapter-11-12.pdf#page=24&selection=10,12,26,6&color=yellow|STT-2920-Chapter-11-12, p.24]])

**Solution: ** [[STT-2920-Chapter-11-12.pdf#page=24&selection=0,50,293,14&color=yellow|STT-2920-Chapter-11-12, p.24]]

### Estimation par IC de la moyenne μ d’une loi normale lorsque  est inconnu
([[STT-2920-Chapter-11-12.pdf#page=25&selection=0,31,8,11&color=yellow|STT-2920-Chapter-11-12, p.25]])

$$\frac{\bar{X}-\mu}{\frac{S}{\sqrt{ n }}} \sim t_{n-1}$$

##### Loi de Student
$$f_{x}(t)=\frac{\Gamma\left( \frac{k+1}{2} \right)}{\Gamma\left( \frac{k}{2} \right)\sqrt{ k\pi }} \frac{1}{(1+\frac{t^{2}}{k})^{(k+1)/2}}$$
$$\mathbb{E}=0 \qquad \mathbb{V}\text{ar}[X]=\frac{k}{k-2}$$
La table fonctionne comme celle du khi_2

###### Proposition 6 (IC pour μ dans le cas d’une population mère normale avec  inconnu)
ans le cas d’une population mère normale avec μ inconnu et  inconnu, l’intervalle de confiance pour μ au niveau de confiance 1 - a est de la forme :
$$\left[ \bar{x}-t_{\frac{\alpha}{2}, n-1} \frac{s}{\sqrt{ n }};\bar{x}+t_{\frac{\alpha}{2}, n-1} \frac{s}{\sqrt{ n }} \right]$$
([[STT-2920-Chapter-11-12.pdf#page=29&selection=0,1,20,15&color=yellow|STT-2920-Chapter-11-12, p.29]])

### I.C. pour μ dans le cas d’une population mère quelconque avec n grand
([[STT-2920-Chapter-11-12.pdf#page=31&selection=0,0,8,5&color=yellow|STT-2920-Chapter-11-12, p.31]])

En invoquant le théorème central limite:
Dans le cas d’une population mère quelconque, si n est grand, l’intervalle suivant est un intervalle de confiance approximatif pour $\mu$ au niveau de confiance $1 - \alpha$ :

Où b doit être estimé à partir de l’échantillon, on prendra en général $\hat{\sigma} = s$.
([[STT-2920-Chapter-11-12.pdf#page=31&selection=18,3,95,1&color=yellow|STT-2920-Chapter-11-12, p.31]])

##### Estimation de la différence de deux moyennes $μ1 - μ2$
([[STT-2920-Chapter-11-12.pdf#page=32&selection=0,44,8,1&color=yellow|STT-2920-Chapter-11-12, p.32]])
Il arrive souvent que l’on souhaite, à partir de deux échantillons, inférer sur la comparaison de deux paramètres des populations respectives sous-jacentes des échantillons, par exemple la comparaison de deux moyenne. Le contexte général est le suivant : 
On a un premier échantillon $X_{1}, X_{2}, . . . , X_{n_{1}}$ provenant de la population 1 (modèle probabiliste 1) de paramètres $μ1$ et $1$. 
On a un deuxième échantillon $Y1, Y2, . . . , Yn2$ provenant de la population 2 (modèle probabiliste 2) de paramètres $μ2$ et $2$. 
Naturellement, un bon estimateur pour l’écart entre $μ1 - μ2$ sera $\bar{X} - \bar{Y}$. 
Or, la distribution d’échantillonnage de la variable aléatoire $\bar{X} -\bar{Y}$, et les formules donnant l’I.C. pour $μ1 - μ2$ dépendra de la distribution de la population mère et de la connaissance ou non des valeurs de $\sigma^{1}$ et $\sigma^{2}$. Les cas typiques que nous rencontrerons se résument dans la proposition suivante.
([[STT-2920-Chapter-11-12.pdf#page=32&selection=10,0,119,81&color=yellow|STT-2920-Chapter-11-12, p.32]])