---
name: Factorisation PTLU
aliase: Fatorisation aigue
type: Matière
---
#MAT-2930 

La factorisation aïgue ou encore la factorisation PTLU est une façons de simplifier les calcule permettant de résoudre un système d'équations.

### Définition
---
La factorisation PTLU est une "décomposition" de la matrice a résoudre:
$$\begin{array}{ccccc}
\left[\begin{array}{ccc}
1&2&1\\
3&8&1\\
0&4&1\\
\end{array}\right]
&
=
&
\left[\begin{array}{ccc}
0&0&1\\
0&1&0\\
1&0&0\\
\end{array}\right]
&
\left[\begin{array}{ccc}
1&0&0\\
3&1&0\\
0&2&1\\
\end{array}\right]
&
\left[\begin{array}{ccc}
1&2&1\\
0&2&-2\\
0&0&5\\
\end{array}\right]\\
A &&P^{T}& L & U
\end{array}
$$

### Résolution avec une factorisé PTLU
---
**Étape 2**: $P\vec{b} = \vec{b'}$
**Étape 2**: $L\vec{y} = \vec{b'}$
**Étape 3**: $U\vec{x} = \vec{y}$