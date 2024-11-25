---
name: Théorème du résidus
type: Matière
---
#GEL-1000 
***
Le théorème du résidu est une façons de calculer L'[[Transformation de Laplace inverse|inverse de la transformation Laplace]].

 > [!Tip] Insight
 > Le théorème des résidus stipule que $f(t)$ est donné par la somme des résidus de $F(s)e^{st}$ . 
 > ([[Chapitre-6.pdf#page=21&selection=4,0,9,1&color=yellow|Chapitre-6, p.21]])

### Mise en place
---
$F(s)$ peut être représentée comme un rapport du polynôme numérateur $N(s)$ au polynôme dénominateur $D(s)$: 
$$F(s) = \frac{N(s)}{D(s)}$$
([[Chapitre-6.pdf#page=21&selection=13,0,14,64&color=yellow|Chapitre-6, p.21]])

> [!Note]
> Les [[Théorème du résidus#Pôle simple|pôle]] ici sont les racine du dénominateur

##### Pôle simple
Si $F(s)$ a un pôle simple en $s = – a$, $D(s) = (s + a)D1(s)$. Le résidu à $s = – a$ est donné par
$$R = \left. (s+a) \frac{N(s)e^{st}}{(s+a)D_{1}(s)}\right|_{s=-a} \implies \frac{N(-a)e^{-at}}{D_{1}(-a)}$$
([[Chapitre-6.pdf#page=21&selection=18,0,19,21&color=yellow|Chapitre-6, p.21]])
##### Pôle multiple
Si $F(s)$ a $r$ pôles à $s = – a$, $D(s) = (s + a)^{r} D1(s)$. Le résidu à $s = – a$ est donné par
$$R = \frac{1}{(r-1)!} \frac{d^{r-1}}{ds^{r-1}} \left. \left[ (s+a)^{r} \frac{N(s)e^{st}}{(s+a)^{r}D_{1}(s)} \right] \right|_{s=-a} \implies \frac{1}{(r-1)!} \frac{d^{r-1}}{ds^{r-1}} \left. \left[\frac{N(s)e^{st}}{D_{1}(s)} \right] \right|_{s=-a} $$
([[Chapitre-6.pdf#page=21&selection=23,0,30,13&color=yellow|Chapitre-6, p.21]])

##### Pôle complexe


### Procédure de résolution
---
Procédure de transformation de Laplace inverse : 
1. Multipliyer le numérateur par $e^{st}$: $F(s) e^{st} = \frac{N(s)e^{st}}{D(s)}$
2. Factoriser $D(s)$ le dénominateur
3. Trouver les residus (Formule ci-haut)
4. Prendre la somme des residus
([[Chapitre-6.pdf#page=21&selection=34,0,56,32&color=yellow|Chapitre-6, p.21]])
