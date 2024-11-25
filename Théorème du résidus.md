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
##### Pôle simple
Si $F(s)$ a un pôle simple en $s = – a$, $D(s) = (s + a)D1(s)$. Le résidu à $s = – a$ est donné par
([[Chapitre-6.pdf#page=21&selection=18,0,19,21&color=yellow|Chapitre-6, p.21]])

##### Pôle multiple

### Procédure de résolution
---
Procédure de transformation de Laplace inverse :  (a) F(s) est = N(s) est /D(s)  (b) Factoriser D(s);  (c) Trouver les residus  (d) Prendre la somme des residus
([[Chapitre-6.pdf#page=21&selection=34,0,56,32&color=yellow|Chapitre-6, p.21]])