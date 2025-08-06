## [1]
$$
\begin{align*}
P(A_j|B) &= \frac{P(A_j, B)}{P(B)}\\
&= \frac{P(B|A_j)P(A_j)}{P(B)}\\
&= cP(B|A_j)
\end{align*}
$$
ただし、$c = P(A_j)/P(B)$ とおいた

## [2]
最初に箱 $i$ を選ぶ事象を $C_i$ とする  
箱 $j$ が当たりの事象を $A_j$ とする  
箱 $k$ が開けられる事象を $B_k$ とする

箱3が開けられたとき、箱2が当たりである確率は、
$$
\begin{align*}
P(A_2 | B_3, C_1) &= \frac{P(A_2, B_3, C_1)}{P(B_3, C_1)}\\
&= \frac{P(B_3 | A_2, C_1)P(A_2 | C_1)P(C_1)}{P(B_3|C_1)P(C_1)}\\
&= \frac{P(B_3 | A_2, C_1)P(A_2 | C_1)}{P(B_3|C_1)}
\end{align*}
$$

- 箱1を選んだときに、箱2が当たりの確率は、$P(A_2|C_1) = 1/3$ (選んだ箱と当たりは関係ない)
- 箱1を選んだときに、箱3が開けられる確率は、
$$
\begin{align*}
P(B_3|C_1) &= \sum_{j=1}^3 P(B_3|A_j, C_1)P(A_j|C_1)\\
&= \frac{1}{3}P(B_3|A_1, C_1) + \frac{1}{3}P(B_3|A_2, C_1) + \frac{1}{3}P(B_3|A_3, C_1)
\end{align*}
$$

問題文から、和夫が選ばなかった2つの箱(2, 3)の中のうち、令美がどちらを選ぶかのルールは読み取れない  
(箱1が外れだったときに、残りの2つのうち外れを開けるとは書かれていない)  
2, 3の箱のどちらを選ぶかは等しく $1/2$ と考える  
したがって
$$
\begin{align*}
P(B_3|A_1, C_1) = P(B_3|A_2, C_1) = P(B_3|A_3, C_1) = \frac{1}{2}
\end{align*}
$$

$$
\begin{align*}
P(A_2 | B_3, C_1) &= \frac{P(B_3 | A_2, C_1)P(A_2 | C_1)}{P(B_3|C_1)}\\
&= \frac{1/2 \cdot 1/3}{1/2}\\
&= \frac{1}{3}
\end{align*}
$$

もし、箱1が外れだったとき、令美は必ず外れの箱を開けるというルールがある場合は、  
$$
\begin{align*}
P(B_3|A_1, C_1) &= \frac{1}{2}\\
P(B_3|A_2, C_1) &= 1\\
P(B_3|A_3, C_1) &= 0\\
P(B_3|C_1) &= \frac{1}{3}\cdot\frac{1}{2} + \frac{1}{3}\cdot 1 + \frac{1}{3}\cdot 0 = \frac{1}{2}\\
P(A_2 | B_3, C_1) &= \frac{P(B_3 | A_2, C_1)P(A_2 | C_1)}{P(B_3|C_1)}\\
&= \frac{1 \cdot 1/3}{1/2}\\
&= \frac{2}{3}
\end{align*}
$$

## [3]
「令美は当たりの箱を開けることがない」という前提を置く
$$
\begin{align*}
P(B_3|A_1, C_1) &= w\\
P(B_3|A_2, C_1) &= 1\\
P(B_3|A_3, C_1) &= 0\\
P(B_3|C_1) &= \frac{1}{3}w + \frac{1}{3}\cdot 1 + \frac{1}{3}\cdot 0 = \frac{1}{3}(1 + w)\\
P(A_2 | B_3, C_1) &= \frac{P(B_3 | A_2, C_1)P(A_2 | C_1)}{P(B_3|C_1)}\\
&= \frac{1 \cdot 1/3}{\frac{1}{3}(1+w)}\\
&= \frac{1}{1+w}
\end{align*}
$$

## [4]
二項分布の確率関数は,
$$
P(X=x) = \binom{n}{x}p^x(1-p)^{n-x}
$$

5%棄却域が $X \ge n-1$ となるとき、
$$
\begin{align*}
P(X \ge n-1 | p=1/2) &= P(X=n | p=1/2) + P(X=n-1 | p=1/2)\\
&= \binom{n}{n}\left(\frac{1}{2}\right)^x\left(\frac{1}{2}\right)^{n-x} + \binom{n}{n-1}\left(\frac{1}{2}\right)^x\left(\frac{1}{2}\right)^{n-x}\\
&= (1 + n)\left(\frac{1}{2}\right)^n \le 0.05
\end{align*}
$$
上式を満たす最小の $n$ は $8$ ($n_0 = 8$)

対立仮説 $p=2/3$ が正しいとき、 $X\ge7$ となる確率は、
$$
\begin{align*}
P(X \ge 7 | p=2/3) &= P(X=8 | p=2/3) + P(X=7 | p=2/3)\\
&= \binom{8}{8}\left(\frac{2}{3}\right)^8\left(\frac{1}{3}\right)^0 + \binom{8}{7}\left(\frac{2}{3}\right)^7\frac{1}{3}\\
& \fallingdotseq 0.195
\end{align*}
$$
検出力は $19.5$ %