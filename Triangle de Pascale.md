---
name: Triangle de pascale
type: Matière
---
#STT-2920

Le triangle de pascale est une exercise mathématique qui a un impacte dans plusieurs domaine.
$$
\array{
&&&&&1&&&&&\\
&&&&1&&1&&&&\\
&&&1&&2&&1&&&\\
&&1&&3&&3&&1&&\\
&1&&4&&6&&4&&1&\\
1&&5&&10&&10&&6&&1\\
}
$$

### Implication polynomial
---
$$
\array{
&&&&&1a^0b^0&&&&&\\
&&&&1a^0b^1&&1a^1b^0&&&&\\
&&&1a^0b^2&&2a^1b^1&&1a^2b^0&&&\\
&&1a^0b^3&&3a^1b^2&&3a^2b^1&&1a^3b^0&&\\
&1a^0b^4&&4a^1b^3&&6a^2b^2&&4a^3b^1&&1a^4b^0&\\
1a^0b^0&&5a^1b^4&&10a^2b^3&&10a^3b^2&&6a^4b^1&&1a^5b^0\\
}
$$

#### Théorème de Newton
Le théorème de Newton permet de trouver la valeur d'un coefficient sans connaitre le triangle en entier
$$(a+b)^{n} = \sum_{k=0}^{n}{n \choose k}a^{k}b^{n-k}$$

### Implication selon les coefficient binomial
$$
\array{
&&&&&{0 \choose 0}&&&&&\\
&&&&{1 \choose 0}&&{1 \choose 1}&&&&\\
&&&{2 \choose 0}&&{2 \choose 1}&&{2 \choose 2}&&&\\
&&{3 \choose 0}&&{3 \choose 1}&&{3 \choose 2}&&{3 \choose 3}&&\\
&{4 \choose 0}&&{4 \choose 1}&&{4 \choose 2}&&{4 \choose 3}&&{4 \choose 4}&\\
{5 \choose 0}&&{5 \choose 1}&&{5 \choose 2}&&{5 \choose 3}&&{5 \choose 4}&&{5 \choose 5}\\
}
$$

> [!Info] Remarque
> - $n$ est équivalent a la ligne
> - $k$ est équivalent à la colonne