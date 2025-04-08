## [1]
$$\begin{align*}
E[X_i] &= \sum_{x=0}^1 x\cdot P(X_i=x) \\
&= 1\cdot P(X_i=1) + 0\cdot P(X_i=0)\\
&= P(X_i=1)
\end{align*}$$
非復元抽出であっても、個々の$X_i$単独で見ると箱全体からのランダム抽出と同じ確率になるので
$$P(X_i=1) = \frac{6}{10} = \frac{3}{5}$$
> 全てのボールをランダムに一列に並べ替える場合を考える。このとき$i$番目のボールが赤である確率は箱の中からランダムにボールを取り出した時に赤である確率と同じになる

また、$E[X_i^2] = \frac{3}{5}$より
$$\begin{align*}
V[X_i] &= E[X_i^2] - E[X_i]^2 \\
&= \frac{3}{5}(1 - \frac{3}{5})\\
&= \frac{6}{25}
\end{align*}$$

## [2]
$$\begin{align*}
E[X_iX_j] &= P(X_i=1, X_j=1)\\
&= \frac{6}{10} \cdot \frac{5}{9}\\
&= \frac{1}{3}
\end{align*}$$

$$\begin{align*}
Cov[X_i, X_j] &= E[X_iX_j] - E[X_i]E[X_j]\\
&= \frac{1}{3} - \left(\frac{6}{10}\right)^2\\
&= -\frac{2}{75}
\end{align*}$$

$$\begin{align*}
R[X_i, X_j] &= \frac{Cov[X_i, X_j]}{\sqrt{V[X_i]V[X_j]}}\\
&= \frac{-\frac{2}{75}}{\sqrt{\frac{6}{25} \cdot\frac{6}{25}}}\\
&= -\frac{1}{9}
\end{align*}$$

## [3]
$$\begin{align*}
E[T_5] &= E[X_1 + X_2 + \cdots + X_5]\\
&= E[X_1]+ E[X_2] + \cdots + E[X_5] \quad(期待値の線形性)\\
&= \frac{3}{5} \cdot 5\\
&= 3
\end{align*}$$

$$\begin{align*}
V[T_5] &= V[X_1 + X_2 + \cdots + X_5]\\
&= V[X_1] + V[X_2] + \cdots + V[X_5] \\
&\quad + 2Cov[X_1, X_2] + 2Cov[X_1, X_3] + \cdots + 2Cov[X_4, X_5]\\
&= \frac{6}{25}\cdot 5 -2\cdot \frac{2}{75}\cdot 10\\
&= \frac{50}{75}\\
&= \frac{2}{3}
\end{align*}$$

## [4]
$$\begin{align*}
P(T_5|M=6) &= \frac{6}{10} \cdot \frac{5}{9} \cdot \frac{4}{8} \cdot \frac{3}{7} \cdot \frac{2}{6} \\
&= \frac{1}{42}
\end{align*}$$

## [5]
Mは5, 6, 7, 8, 9, 10の可能性があり、$P(T_5=5|M)$を有意水準5%で棄却しない最小のMを探索する  

$$\begin{align*}
P(T_5|M=5) &= \frac{5}{10} \cdot \frac{4}{9} \cdot \frac{3}{8} \cdot \frac{2}{7} \cdot \frac{1}{6} \\
&= \frac{1}{252}\\
&= 0.00397
\end{align*}$$

$$\begin{align*}
P(T_5|M=6) &= \frac{6}{10} \cdot \frac{5}{9} \cdot \frac{4}{8} \cdot \frac{3}{7} \cdot \frac{2}{6} \\
&= \frac{1}{42}\\
&= 0.0238
\end{align*}$$

$$\begin{align*}
P(T_5|M=7) &= \frac{7}{10} \cdot \frac{6}{9} \cdot \frac{5}{8} \cdot \frac{4}{7} \cdot \frac{3}{6} \\
&= \frac{1}{12}\\
&= 0.0833
\end{align*}$$
