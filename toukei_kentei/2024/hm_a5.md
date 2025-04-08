## [1]

$$\begin{align*}
\begin{pmatrix}
1 & r_{12} \\ r_{12} & 1
\end{pmatrix}\begin{pmatrix}
b_1 \\ b_2
\end{pmatrix} &= \begin{pmatrix}
r_{y1} \\ r_{y2}
\end{pmatrix}\\
\begin{pmatrix}
b_1 + r_{12}b_2 \\ r_{12}b_1 + b_2
\end{pmatrix} &= \begin{pmatrix}
r_{y1} \\ r_{y2}
\end{pmatrix}\\
\begin{pmatrix}
b_1 + 0.5b_2 \\ 0.5b_1 + b_2
\end{pmatrix} &= \begin{pmatrix}
0.6 \\ 0
\end{pmatrix}
\end{align*}$$

$\therefore$ $b_1 = 0.8$, $b_2 = -0.4$

## [2]
[1]二式目より $b_2 = r_{y2} - r_{12}b_1$  
[1]一式目に代入する
$$\begin{align*}
&b_1 +r_{12}(r_{y2} - r_{12}b_1) = r_{y1}\\
&(1-r_{12}^2)b_1 + r_{12}r_{y2} = r_{y1}\\
&b_1 = \frac{r_{y1} - r_{12}r_{y2}}{1 - r_{12}^2}
\end{align*}$$
$b_1 \gt r_{y1}$となるためには、
$$\begin{align*}
b_1 - r_{y1} &\gt 0\\
\frac{r_{y1} - r_{12}r_{y2}}{1 - r_{12}^2} - r_{y1} &\gt 0\\
r_{y1} - r_{12}r_{y2} - r_{y1}(1 - r_{12}^2)&\gt 0\\
r_{y1}r_{12}^2 - r_{y2}r_{12}&\gt 0\\
(r_{y1}r_{12} - r_{y2})r_{12}&\gt 0\\
\therefore r_{12}\gt \frac{r_{y2}}{r_{y1}}
\end{align*}$$

## [3]
[1]一式目より $b_1 = r_{y1} - r_{12}b_2$  
[1]二式目に代入する
$$\begin{align*}
&r_{12}(r_{y1} - r_{12}b_2) + b_2 = r_{y2}\\
&(1 - r_{12}^2)b_2 + r_{12}r_{y1} = r_{y2}\\
&b_2 = \frac{r_{y2} - r_{12}r_{y1}}{1 - r_{12}^2}
\end{align*}$$
$r_{y2}\ge0$かつ$b_2 \lt 0$となるためには、
$$\begin{align*}
\frac{r_{y2} - r_{12}r_{y1}}{1 - r_{12}^2} \lt 0\\
r_{y2} - r_{12}r_{y1}\lt 0\\
r_{12} \gt \frac{r_{y2}}{r_{y1}}
\end{align*}$$

## [4]
$$\begin{align*}
V[\hat{y}] &= V[0.8x_1 -0.4x_2]\\
&= 0.8^2V[x_1] + 0.4^2V[x_2] - 2\cdot0.8\cdot0.4Cov[x_1, x_2]\\
&= 0.64 + 0.16 - 0.64 * 0.5\\
&= 0.48
\end{align*}$$

$$\begin{align*}
Cov[y, \hat{y}] &= E[y\hat{y}] - E[y]E[\hat{y}]\\
&= E[y(0.8x_1 -0.4x_2)]\\
&= 0.8E[x_1y] - 0.4E[x_2y]\\
&= 0.8(Cov[x_1, y] + E[x_1]E[y]) - 0.4(Cov[x_2, y] + E[x_2]E[y])\\
&= 0.8 * 0.6 - 0.4 * 0\\
&= 0.48
\end{align*}$$

## [5]
$R^2$は$y$と$\hat{y}$の相関係数の二乗
$$\begin{align*}
\rho &= \frac{Cov[y, \hat{y}]}{\sqrt{V[y]V[\hat{y}]}}\\
&= \frac{0.48}{\sqrt{1*0.48}}\\
&= \sqrt{0.48}
\end{align*}$$
したがって
$$
R^2 = \rho^2 = \sqrt{0.48}^2
 = 0.48$$
