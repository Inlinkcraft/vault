---
name: Cours-10
type: Class
course: GEL-1000
date: 2024-10-11T09:30
Complete: true
---
#school/GEL-1000  
***

# Exemple de résolution de circuit complexe

```circuitjs
$ 1 0.000005 14.235633750745258 55 5 50 5e-11
r 176 80 336 80 0 1000
c 336 80 336 256 0 0.000032999999999999996 4.999999999989941 0.001
s 176 80 176 256 0 0 false
v 336 256 176 256 0 0 40 5 0 0 0.5
o 1 64 0 4099 5 0.05 0 2 1 3
38 1 F1 0 0.000001 0.000101 -1 Capacitance
```

## Résolution

##### Maille-ish
$$
\begin{array}{rcll}
V_s&=&V_{c} + V_{R}&\\
V_s&=&V_{c} + Ri & \text{Le courant ici est le même dans la maille et le condensateur}\\
V_s&=&V_{c} + RC\frac{dV_{c}}{dt} & \text{On a tous en fonction de } V_c\\
\end{array}
$$
##### Résolution de l'équation différentielle
###### Homogène
$$
\begin{array}{rcll}
V_{c} + RC\frac{dV_{c}}{dt}&=&0&\\
RC\frac{dV_{c}}{dt}&=&- V_{c}&\\
RC \ dV_{c}&=&- V_{c} \ dt&\\
RC\frac{1}{V_{c}} \ dV_{c}&=&-dt&\\
\frac{1}{V_{c}} \ dV_{c}&=&\frac{-1}{RC}dt&\\
\int\frac{1}{V_{c}} \ dV_{c}&=&\int\frac{-1}{RC}dt&\\
\ln (V_{c})&=&\frac{-1}{RC}t + K&\\
V_{c}&=&e^{\frac{-1}{RC}(t + K)}&\\
V_{c}&=&e^{\frac{-t}{RC}} \cdot e^{\frac{-K}{RC}}& (e^{\frac{-K}{RC}} \text{ est une constante... on la remplace par }C)\\
V_{ch}&=&Ce^{\frac{-t}{\tau}}& \text{où la constante de temps } \tau = RC\\
\end{array}
$$
###### Particulière
$$
\begin{array}{rcll}
V_{c} & = & V_{ch} + V_{cp}&\\
V_{c} & = & Ce^{\frac{-t}{\tau}} + V_{cp}&\\
\text{C.I. à } t=0&:&V_{c}= 0&\\
V_{c}(0) & = & Ce^{\frac{-0}{\tau}} + V_{cp}&\\
0 & = & Ce^{0} + V_{cp}&\\
0 & = & C\cdot1 + V_{cp}&\\
C & = & -V_{cp}&\\
\end{array}
$$
###### Solution
$$
\begin{array}{rcll}
V_{c} & = & V_{ch} + V_{cp}&\\
V_{c} & = & -V_{cp}e^{\frac{-t}{\tau}} + V_{cp}&\\
V_{c} & = & V_{cp}(-e^{\frac{-t}{\tau}} + 1)&\\
V_{c} & = & V_{cp}(1 - e^{\frac{-t}{\tau}})&\\
V_{c} & = & V_{s}(1 - e^{\frac{-t}{\tau}})& \text{ici } V_{s}= V_{cp}\\
\end{array}
$$

# Évaluation du TP2
```circuitjs
$ 1 0.000005 1.0312258501325766 36 5 50 5e-11
l 384 176 384 272 0 0.5 0.008571428571428476 0
l 464 176 464 272 0 0.2 0.02142857142857106 0
r 160 96 224 96 0 400
r 304 176 304 272 0 1300
w 464 272 384 272 0
w 384 272 304 272 0
w 304 272 160 272 0
v 160 272 160 96 0 0 40 12 0 0 0.5
370 304 128 304 176 1 0 0
370 384 128 384 176 1 0 0
370 464 128 464 176 1 0 0
370 272 96 224 96 1 0 0
207 384 96 384 64 4 V_L
w 272 96 304 96 0
w 304 128 304 96 0
w 384 128 384 96 0
w 384 96 464 96 0
w 464 128 464 96 0
x 185 72 199 75 4 8 R_1
x 240 73 250 76 4 8 i_s
x 316 213 330 216 4 8 R_2
x 315 139 325 142 4 8 i_0
x 395 140 405 143 4 8 i_1
x 396 212 409 215 4 8 L_1
x 475 142 485 145 4 8 i_2
x 476 211 489 214 4 8 L_2
w 304 96 384 96 0
x 122 180 135 183 4 8 V_s
x 114 195 145 198 4 12 12u(t)
o 7 1 0 4099 20 0.05 0 2 7 3
o 1 1 0 4099 0.0000762939453125 0.025 1 2 1 3
```

## Résolution

#### Équation de maille
$$
\begin{array}{rcll}
V_s(t)&=&R_1(j_{1}) + R_2(j_{1}-j_{2})& \\
0&=&R_2(j_{2}-j_{1}) + L_1(\frac{d(j_{2} - j_{3})}{dt})& \\
0&=&L_1\left(\frac{d(j_{3} - j_{2})}{dt}\right) + L_2\frac{d(j_3)}{dt}& \\
\end{array}
$$

#### Équation de nœud
$$
\begin{array}{rcll}
\frac{V_L-V_s}{R_{1}} + \frac{V_L}{R_{2}} + \frac{1}{L_{1}} \int V_{L} \ dt+ \frac{1}{L_{2}}\int V_{L} \ dt&=&0&\\
\end{array}
$$
##### Simplification
$$
\begin{array}{rcll}
\frac{V_L}{R_{1}} - \frac{V_s}{R_{1}} + \frac{V_L}{R_{2}} + \frac{1}{L_{1}} \int V_{L} \ dt+ \frac{1}{L_{2}}\int V_{L} \ dt&=&0 &\\
\frac{V_L}{R_{1}} + \frac{V_L}{R_{2}} + \frac{1}{L_{1}} \int V_{L} \ dt+ \frac{1}{L_{2}}\int V_{L} \ dt &=& \frac{V_s}{R_{1}} &\\
(\frac{1}{R_{1}} + \frac{1}{R_{2}})V_L + (\frac{1}{L_{1}} + \frac{1}{L_{2}})\int V_{L} \ dt &=& \frac{V_s}{R_{1}} &\\
\end{array}
$$

##### Résolution selon ma tête
$$
\begin{array}{rcll}
(\frac{1}{R_{1}} + \frac{1}{R_{2}})V_L + (\frac{1}{L_{1}} + \frac{1}{L_{2}})\int V_{L} \ dt &=& \frac{V_s}{R_{1}} &\\
(\frac{1}{R_{1}} + \frac{1}{R_{2}})\frac{dV_L}{dt} + (\frac{1}{L_{1}} + \frac{1}{L_{2}}) V_{L} &=& \frac{1}{R_{1}}\frac{dV_s}{dt} &\\
(\frac{1}{R_{1}} + \frac{1}{R_{2}})\frac{dV_L}{dt} + (\frac{1}{L_{1}} + \frac{1}{L_{2}}) V_{L} &=& \frac{12}{R_{1}}\delta(t) & \text{car } \frac{dV_{s}}{dt} = 12\delta(t)\\
\end{array}
$$

###### Homogène
$$
\begin{array}{rcll}
(\frac{1}{R_{1}} + \frac{1}{R_{2}})\frac{dV_L}{dt} + (\frac{1}{L_{1}} + \frac{1}{L_{2}}) V_{L} &=& 0 &\\
(\frac{1}{R_{1}} + \frac{1}{R_{2}})\frac{dV_L}{dt} &=& - (\frac{1}{L_{1}} + \frac{1}{L_{2}}) V_{L} &\\
\frac{(\frac{1}{R_{1}} + \frac{1}{R_{2}})dV_L}{- (\frac{1}{L_{1}} + \frac{1}{L_{2}}) V_{L}} &=& 1 \ dt&\\
\frac{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})} \frac{dV_L}{V_{L}} &=& dt&\\
\frac{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})} \int \frac{1}{V_{L}}dV_{L} &=& \int dt&\\
\frac{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})} \ln{V_{L}} &=& t + K&\\
\ln{V_{L}} &=& \frac{t + K}{\frac{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}}&\\
\ln{V_{L}} &=& \frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t) + K& \text{ici } K \text{ absorbe les constante}\\
V_{L} &=& Ke^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)}& \text{ici } K \text{ absorbe les constante}\\
V_{L} &=& Ke^{\sigma(t)}& \text{ici } \sigma = \frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}\\
\text{si } \tau & = &\frac{-1}{\sigma}& \text{Donc } \tau = \frac{-1}{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}} \\
\tau &=& {\frac{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}{(\frac{1}{L_{1}} + \frac{1}{L_{2}})}} \\
V_{Lh} &=& Ke^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}}& \text{solution homogène}\\
\end{array}
$$

###### Donc particulière
$$C.I.: \qquad t = 0 \qquad V_{s}(0) = 12\delta(0) = 12 \qquad V_{L}(0) = \frac{1300}{400+1300}V_{s}(0)=\frac{156}{17}$$
$$
\begin{array}{rcll}
V_{Lh} &=& Ke^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)}& \text{solution homogène}\\
V_{L}(t) &=& Ke^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)}& \text{sachant } V_{L}(0) = \frac{156}{17}\\
\frac{156}{17} &=& Ke^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(0)}& \text{sachant } V_{L}(0) = \frac{156}{17}\\
\frac{156}{17} &=& Ke^{0} + V_{Lp}(0)&\\
\frac{156}{17} &=& K(1) + V_{Lp}(0)&\\
\frac{156}{17} &=& K + V_{Lp}(0)&\\
\frac{156}{17} &=& K&\\
V_{L}(t)&=& (\frac{156}{17})e^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)} &\\
\end{array}
$$

###### Trouvons le courant
$$
\begin{array}{rcll}
i_{L}(t)&=& (\frac{1}{L_2})\int{(\frac{156}{17})e^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)}} dt &\\
i_{L}(t)&=& (\frac{1}{L_2})(\frac{156}{17})\int{e^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)}} dt &\\
& & & \\
\text{Poson:}& & & \\
u = {\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}t} & du = {\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}dt} & dt = {\frac{- (\frac{1}{R_{1}} + \frac{1}{R_{2}})}{(\frac{1}{L_{1}} + \frac{1}{L_{2}})}du}\\
& & & \\
i_{L}(t)&=& (\frac{1}{L_2})(\frac{156}{17})\int{e^{u}} \ {\frac{- (\frac{1}{R_{1}} + \frac{1}{R_{2}})}{(\frac{1}{L_{1}} + \frac{1}{L_{2}})}du} & \\
i_{L}(t)&=& (\frac{1}{L_2})(\frac{156}{17})(\frac{- (\frac{1}{R_{1}} + \frac{1}{R_{2}})}{(\frac{1}{L_{1}} + \frac{1}{L_{2}})})\int{e^{u}} \ du & \\
i_{L}(t)&=& (\frac{1}{L_2})(\frac{156}{17})(\frac{- (\frac{1}{R_{1}} + \frac{1}{R_{2}})}{(\frac{1}{L_{1}} + \frac{1}{L_{2}})})(e^{u} + K)& \\
i_{L}(t)&=& (\frac{1}{0.2})(\frac{156}{17})(\frac{- (\frac{1}{R_{1}} + \frac{1}{R_{2}})}{(\frac{1}{L_{1}} + \frac{1}{L_{2}})})e^{{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}t}} + K& \\
i_{L}(t)&=& \frac{-3}{140}e^{{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}t}} + K& \\
0&=& \frac{-3}{140}e^{{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}0}} + K& \text{sachant } i_{L}(0)= 0\\
i_{L}(t)&=& \frac{-3}{140}e^{{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}t}} + K& \\
0&=& \frac{-3}{140}e^{0} + K& \\
0&=& \frac{-3}{140}(1) + K& \\
\frac{3}{140} &=&  K& \\
i_{L}(t)&=& \frac{-3}{140}e^{{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}t}} + \frac{3}{140}& \\
\end{array}
$$

###### Suite TP2
$$
\begin{array}{rcll}
V_{s1} &=& 12 u(t) &\\
V_{s2} &=& 3 \delta(t-1\times 10 ^{-3}) &\\
V_{s1} \to V_{s2} &=& \frac{\frac{dV_{s1}}{{dt}}}{4} & \text{Donc :}\\
V_{L} &=& \frac{1}{4}\frac{d}{dt}\left((\frac{156}{17})e^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)} \right)&\\
V_{L} &=& (\frac{1}{4}\frac{156}{17})\left(e^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)} \cdot {\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}}\right)&\\
V_{L} &=& (\frac{156}{68})e^{\frac{- (\frac{1}{L_{1}} + \frac{1}{L_{2}})}{(\frac{1}{R_{1}} + \frac{1}{R_{2}})}(t)} \cdot {\frac{- 156(\frac{1}{L_{1}} + \frac{1}{L_{2}})}{68(\frac{1}{R_{1}} + \frac{1}{R_{2}})}}&\\
\end{array}
$$