---
name: Tp4
type: Evaluation
course: GEL-1000
date: 2024-11-29T23:59
ponderation: 2
note:
status: En cours
---
#school/GEL-1000
- [ ] TP4 Circuit - 📅 2024-11-29
      [clock::2024-11-26T16:52:36]

> [!PDF|yellow] [[TP4.pdf#page=1&selection=23,0,151,29&color=yellow|TP4, p.1]]
> La fonction residue retourne trois vecteurs de valeurs contenant respectivement les résidus, les pôles et les termes directes. Il faut appeler cette fonction avec deux arguments. Le premier est un vecteur qui représente les coefficients du polynôme du numérateur et le second, ceux du dénominateur. Par exemple, pour le polynôme $P(s) = s2 + 4$, le vecteur correspondant doit s’écrire sous la forme suivante :
> $P = [1, 0, 4]$ 
> Pour appeler une fonction retournant plusieurs variables, on utilise la commande suivante :
> ```
> [var1, var2, . . . , varn] = nomfonction(arg1, arg2, . . . , argm)
> ```
> Ainsi, pour appeler la fonction residue, il faut le faire de la façon suivante : 
> ```
> [residus, poles, direct] = residue (num, denom)
> ``` 
> Cette fonction est codée de façon à ce que le premier élément du vecteur des résidus est le résidu au pôle du premier élément du vecteur des pôles, et ainsi de suite. Le vecteur direct regroupe les coefficients du polynôme quotient suite à la division polynomiale de num par denom lorsque le degré du numérateur est supérieur ou égal à celui du dénominateur. La fonction conv est très pratique pour effectuer le produit de deux polynômes :
> ```
> polyProd = conv(poly1, poly2)
> ```

### Bien Livrable 
- [ ] Vous devez fournir l’ensemble de vos démarches ou analyses dans un document PDF TP4.pdf. 
- [ ] L’ensemble des réponses doivent être rédigées avec un logiciel de traitement de texte. 
- [ ] Les copies manuscrites ne seront pas corrigées et se verront attribuer la note de 0. 
- [ ] Le nombre de pages autorisées pour ce travail est de 1 en excluant les captures d’écran ; soyez concis. 2
- [ ] Inserez les images de capture faites dans altium en donnant un titre qui réfère clairement à la question. 
- [ ] Vous devez remettre une archive Zip nommée NomPrénom TP4.zip contenant les 2 fichiers demandés ( 1× .pdf et 1× .SchDoc) dans la boite de dépôt du portail du cours.
([[TP4.pdf#page=1&color=note|TP4, p.1]])

### Note et démarche
##### Question 1:

```circuitjs
$ 1 0.000005 382.76258214399064 42 5 43 5e-11
v 80 288 80 192 0 1 1.4323944878 12 0 0 0.5
l 80 192 176 192 0 15 0.25915587772566423 0
l 80 96 176 96 0 10 0.3887338165885242 0
r 176 96 368 96 0 24
i 176 144 368 144 0 0.4
c 176 192 176 288 0 0.17 -0.23510507254974886 0
c 272 192 272 288 0 0.03 -0.23510507254974888 0
r 272 192 368 192 0 12
w 80 192 80 96 0
w 176 192 176 144 0
w 176 144 176 96 0
w 368 96 368 144 0
w 368 144 368 192 0
w 368 192 368 288 0
w 368 288 272 288 0
w 272 288 176 288 0
w 176 288 80 288 0
r 176 192 272 192 0 1e-15
g 224 288 224 304 0 0
o 6 512 0 4099 1.25 0.2 0 2 6 3
o 0 1024 0 4099 20 0.8 1 2 0 3
```

**a): Déterminez d’abord l’expression analytique de $V_{a}(s)$ en supposant que les conditions initiales sont nulles partout sous la forme : 
$$V_{a} = \underbrace{{\frac{P_{1}(s)}{Q(s)}}V_{s}}_{V_{a1}(s)}+\underbrace{\frac{P_{2}(s)}{Q(s)}I_{s}}_{V_{a2}(s)}$$
([[TP4.pdf#page=2&selection=147,0,153,35&color=red|TP4, p.2]])**
    Écrivons le nœud $V_{a}$
$$\begin{array}{l}
0= \\
\underbrace{\frac{V_{a}(s)-V_{s}(s)}{10s}}_{L_{10}}+\underbrace{\frac{V_{a}(s)-V_{s}(s)}{15s}}_{L_{15}}+\underbrace{(V_{a}(s)-V_{ref})0.170s}_{C_{0.170}} + \underbrace{(V_{a}(s)-V_{ref})0.030s}_{C_{0.030}}+\underbrace{\frac{V_{a}(s)-V_{ref}}{12}}_{R_{12}}+I_{s}(s)+\underbrace{\frac{V_{a}(s)-V_{ref}}{24}}_{R_{24}}\\
\frac{V_{a}(s)}{10s}-\frac{V_{s}(s)}{10s}+\frac{V_{a}(s)}{15s}-\frac{V_{s}(s)}{15s}+0.170sV_{a}(s) + 0.030sV_{a}(s)+\frac{V_{a}(s)}{12}+\frac{V_{a}(s)}{24}+I_{s}(s) \\
V_{a}(s)(\frac{1}{10s}+\frac{1}{15s}+0.170s+ 0.030s+\frac{1}{12}+\frac{1}{24})+V_{s}(s)(-\frac{1}{10s}-\frac{1}{15s})+I_{s}(s) \\
\end{array}$$
$$-V_{a}(s)(\frac{1}{10s}+\frac{1}{15s}+0.170s+ 0.030s+\frac{1}{12}+\frac{1}{24})=V_{s}(s)(-\frac{1}{10s}-\frac{1}{15s})+I_{s}(s)$$
$$V_{a}(s)=\frac{-(V_{s}(s)(-\frac{1}{10s}-\frac{1}{15s})+I_{s}(s))}{\frac{1}{10s}+\frac{1}{15s}+0.170s+ 0.030s+\frac{1}{12}+\frac{1}{24}}$$
$$V_{a}(s)=\frac{-V_{s}(s)\left( -\frac{1}{10s}-\frac{1}{15s} \right)-I_{s}(s)}{\frac{1}{s}\left( \frac{1}{10}+\frac{1}{15} \right)+s(0.170 + 0.030)+\frac{3}{24}}$$
$$V_{a}(s)=\frac{-V_{s}(s)\left( -\frac{1}{10s}-\frac{1}{15s} \right)-I_{s}(s)}{\frac{1}{s}\left( \frac{1}{10}+\frac{1}{15} \right)+0.2s+0.125}$$
$$V_{a}(s)=\frac{\frac{1}{6s}V_{s}(s)-I_{s}(s)}{\frac{1}{6s}+0.2s+0.125}$$
$$V_{a}(s)=\frac{\frac{1}{6s}V_{s}(s)}{\frac{1}{6s}+0.2s+0.125}-\frac{I_{s}(s)}{\frac{1}{6s}+0.2s+0.125}$$
> Multiplication par $\frac{s}{s}$

$$V_{a}(s)=\frac{\frac{1}{6}V_{s}(s)}{0.2s^{2}+0.125s+\frac{1}{6}}-\frac{sI_{s}(s)}{0.2s^{2}+0.125s+\frac{1}{6}}$$
$$V_{a}(s)=\frac{\frac{1}{6}}{0.2s^{2}+0.125s+\frac{1}{6}}V_{s}(s)+\frac{-s}{0.2s^{2}+0.125s+\frac{1}{6}}I_{s}(s)$$


**b): À l’aide de Matlab, donnez les pôles et résidus de chacune des fonctions $V_{ak}(s) \ \ (k = 1, 2)$ permettant de déterminer ensuite les expressions analytiques de $v_{a1}(t)$, et $v_{a2}(t)$ séparément. Ajoutez la saisie des commandes et des résultats retournés de l’invite de commande pour l’obtention de $v_{a1}(t)$ (pensez à utiliser la fonction conv). ([[TP4.pdf#page=2&selection=178,0,237,2&color=red|TP4, p.2]])**
    $$V_{s}(s) = \frac{9}{s^{2}+9^{2}} \qquad I_{s}(s) = \frac{0.4}{s}$$
    $$V_{a}(s)=\frac{\frac{1}{6}}{0.2s^{2}+0.125s+\frac{1}{6}}\frac{9}{s^{2}+9^{2}}+\frac{-s}{0.2s^{2}+0.125s+\frac{1}{6}}\frac{0.4}{s}$$
```
RVa1 =

  -3.6290e-04 + 5.1720e-03i
  -3.6290e-04 - 5.1720e-03i
   3.6290e-04 - 5.4402e-02i
   3.6290e-04 + 5.4402e-02i

PVa1 =

        0 + 9.0000i
        0 - 9.0000i
  -0.3125 + 0.8577i
  -0.3125 - 0.8577i

RVa2 =

   0.0000 + 1.1659i
   0.0000 - 1.1659i
        0 +      0i

PVa2 =

  -0.3125 + 0.8577i
  -0.3125 - 0.8577i
        0 +      0i

```

**c): Faites tracer le régime transitoire de $v_{a}(t)$ fourni par le simulateur Altium. 
Exportez l’image pour présenter les résultats obtenus avec Altium. Vous devrez modifier les paramètres de la source pour s’assurer de la bonne fréquence de $\frac{9}{2𝜋}$Hz (et non en rad/s), la bonne phase ($0°$) et un facteur d’amortissement nul. ([[TP4.pdf#page=2&selection=241,0,266,36&color=red|TP4, p.2]])**
     Fait facilement....

##### Question 2:
**On mesure la tension aux bornes d’une inductance dans un circuit linaire. La transformée de Laplace de cette tension s’exprime par :
$$V_{L}{\big(}s{\big)}\!=\!\frac{0.4s^{5}\!+\!12.1s^{4}\!+\!132.8s^{3}+723.8s^{2}\!+\!1993.8s\!+\!2096.1}{s^{5}\!+\!18s^{4}\!+\!142s^{3}+620s^{2}\!+\!1425s\!+\!1250}$$
A l’aide de Matlab (ou Octave), trouvez l’expression analytique de VL(t). Arrondissez à 2 chiffres après le point. Faites une saisie des commandes et des résultats retournés de l’invite de commande de Matlab (ou Octave), et décrivez les étapes menant à votre résultat. ([[TP4.pdf#page=3&selection=28,0,173,1&color=red|TP4, p.3]])**
    