---
name: Characterisation dun système linéaire infinie
type: Matière
---
#MAT-2930 

La characterisation d'un système linéaire infinie se fait en exprimant la [[Matrice|matrice]] en équation linéaire pour ensuite la transformer en [[Vecteur#Combinaison Linéaire|combinaison linéaire]].

### Exemple
---
Soit la [[Matrice|matrice]] suivante:
$$
\left[\begin{array}{ccc|c}
1 & 0 & -3 & 1 \\
0 & 1 & -2 & 2 \\
\end{array}\right]
$$
$$
\begin{array}{c}
x_{1} = 1 + 3x_{3} \\
x_{2} = 2 + 2x_{3} \\
\end{array}
$$
On pose $x_{3}= s$ donc si $x_{3}= 0$:
$$
\begin{array}{c}
x_{1} = 1 + 3(0) = 1 \\
x_{2} = 2 + 2(0) = 2 \\
x_{2} = (0) = 0 \\
\end{array}
$$
Ici, la solution homogène est $x = [1 \quad 2 \quad 0]$ donc la solution est:
$$\left[\begin{array}{c}x \\ y \\ z \end{array}\right] = \left[\begin{array}{c}1 \\ 2 \\ 0 \end{array}\right] + s \left[\begin{array}{c}3 \\ 2 \\ 1 \end{array}\right]$$

