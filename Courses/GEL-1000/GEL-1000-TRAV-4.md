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

```

**a): Déterminez d’abord l’expression analytique de $V_{a}(s)$ en supposant que les conditions initiales sont nulles partout sous la forme : 
$$V_{a} = \underbrace{{\frac{P_{1}(s)}{Q(s)}}V_{s}}_{V_{a1}(s)}+\underbrace{\frac{P_{2}(s)}{Q(s)}I_{s}}_{V_{a2}(s)}$$
([[TP4.pdf#page=2&selection=147,0,153,35&color=red|TP4, p.2]])**
    

**b): À l’aide de Matlab, donnez les pôles et résidus de chacune des fonctions $V_{ak}(s) \ \ (k = 1, 2)$ permettant de déterminer ensuite les expressions analytiques de $v_{a1}(t)$, et $v_{a2}(t)$ séparément. Ajoutez la saisie des commandes et des résultats retournés de l’invite de commande pour l’obtention de $v_{a1}(t)$ (pensez à utiliser la fonction conv). ([[TP4.pdf#page=2&selection=178,0,237,2&color=red|TP4, p.2]])**
    

**c): Faites tracer le régime transitoire de $v_{a}(t)$ fourni par le simulateur Altium. 
Exportez l’image pour présenter les résultats obtenus avec Altium. Vous devrez modifier les paramètres de la source pour s’assurer de la bonne fréquence de $\frac{9}{2𝜋}$Hz (et non en rad/s), la bonne phase ($0°$) et un facteur d’amortissement nul. ([[TP4.pdf#page=2&selection=241,0,266,36&color=red|TP4, p.2]])**
    

##### Question 2:
**On mesure la tension aux bornes d’une inductance dans un circuit linaire. La transformée de Laplace de cette tension s’exprime par :
$$V_{L}{\big(}s{\big)}\!=\!\frac{0.4s^{5}\!+\!12.1s^{4}\!+\!132.8s^{3}+723.8s^{2}\!+\!1993.8s\!+\!2096.1}{s^{5}\!+\!18s^{4}\!+\!142s^{3}+620s^{2}\!+\!1425s\!+\!1250}$$
A l’aide de Matlab (ou Octave), trouvez l’expression analytique de VL(t). Arrondissez à 2 chiffres après le point. Faites une saisie des commandes et des résultats retournés de l’invite de commande de Matlab (ou Octave), et décrivez les étapes menant à votre résultat. ([[TP4.pdf#page=3&selection=28,0,173,1&color=red|TP4, p.3]])**
    