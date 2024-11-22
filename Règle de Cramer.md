---
name: Règle de Cramer
type: Matière
---
#GEL-1000 #MAT-2930 

La règle de Cramer est une méthode rapide et efficace des trouver les valeur du [[Vecteur|vecteur]] inconnue dans une [[Matrice#Représentation matriciel d'une équation linéaire|équation linéaire]].

### Procédure
---
Soit $A\vec{x} = \vec{y}$
$$
\left[\begin{array}{ccc} 
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{array}\right]
\left[\begin{array}{c} 
x_{1} \\
x_{2} \\
x_{3} \\
\end{array}\right]
=
\left[\begin{array}{c} 
y_{1} \\
y_{2} \\
y_{3} \\
\end{array}\right]
$$
Donc:
$$
x_{1}= \frac{\left|\begin{array}{ccc} 
y_{1} & a_{12} & a_{13} \\
y_{2} & a_{22} & a_{23} \\
y_{3} & a_{32} & a_{33} \\
\end{array}\right|}{\left|\begin{array}{ccc} 
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{array}\right|} 
\qquad 
x_{2}= \frac{\left|\begin{array}{ccc} 
a_{11} & y_{2} & a_{13} \\
a_{21} & y_{2} & a_{23} \\
a_{31} & y_{2} & a_{33} \\
\end{array}\right|}{\left|\begin{array}{ccc} 
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{array}\right|} 
\qquad
x_{3}= \frac{\left|\begin{array}{ccc} 
a_{11} & a_{12} & y_{1} \\
a_{21} & a_{22} & y_{2} \\
a_{31} & a_{32} & y_{3} \\
\end{array}\right|}{\left|\begin{array}{ccc} 
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{array}\right|} 
$$