## [1]

$$
\begin{align*}
r_{XY/W} &= \frac{r_{XY} - r_{XW}r_{YW}}{\sqrt{(1-r_{XW}^2)(1-r_{YW}^2)}}\\
&=\frac{0.72 - 0.9\cdot0.8}{\sqrt{(1-0.9^2)(1-0.8^2)}}\\
&=0
\end{align*}
$$
WがXとWの交絡因子になっており、Wの影響を除いたときXとYは無相関である

## [2]

### [2-1]
$$
\begin{align*}
V[X] &= V[r_{XW}W + E_1]\\
&= r_{XW}^2V[W] + V[E_1]\\
V[E_1] &= V[X] - r_{XW}^2V[W]\\
V[E_1] &= 1 - 0.9^2\cdot1\\
&= 0.19\\
\\
V[E_2] &= V[Y] - r_{YW}^2V[W]\\
V[E_2] &= 1 - 0.8^2\cdot1\\
&= 0.36\\
\end{align*}
$$

### [2-2]

$$
\begin{align*}
r_{E_1E_2} &= \frac{Cov(E_1, E_2)}{\sqrt{V[E_1]}{V[E_2]}}\\
\\
Cov(E_1, E_2) &= Cov(X-r_{XW}W, Y-r_{YW}W)\\
&= E[(X-r_{XW}W)(Y-r_{YW}W))] - E[X-r_{XW}W]E[Y-r_{YW}W)]\\
&= E[XY - r_{YW}XW - r_{XW}YW + r_{XW}r_{YW}W^2] - 0\\
&= Cov(X, Y) - r_{YW}Cov(X, W) - r_{XW}Cov(Y, W) + r_{XW}r_{YW}V[W] \quad (\because E[X], E[Y], E[W] = 0)\\
&= r_{XY} - r_{YW}r_{XW} - r_{XW}r_{YW} + r_{XW}r_{YW} \quad (\because V[X], V[Y], V[W] = 1)\\
&= r_{XY} - r_{XW}r_{YW}\\
&= 0.72 - 0.9\cdot0.8\\
&= 0\\
&= r_{XY/W}
\end{align*}
$$

## [3]

平均二乗誤差の期待値 $S_1 = E[(Y - aX)^2]$ を最小化する$a$ を求める

$$
\begin{align*}
\frac{\partial S_1}{\partial a} &= E[-2X(Y - aX)]\\
&= 2aE[X^2] - 2E[XY]\\
\end{align*}
$$

偏微分が $0$ になるとき

$$
\begin{align*}
&aE[X^2] - E[XY] = 0\\
&\Leftrightarrow \\
&a = 0.72
\end{align*}
$$


平均二乗誤差の期待値 $S_2 = E[(Y - b_1X - b_2W)^2]$ を最小化する$b_1$, $b_2$ を求める

$$
\begin{align*}
\frac{\partial S_2}{\partial b_1} &= E[-2X(Y - b_1X - b_2W)]\\
&= 2b_1E[X^2] +2b_2E[XW] -2E[XY]\\
\\
\frac{\partial S_2}{\partial b_2} &= E[-2W(Y - b_1X - b_2W)]\\
&= 2b_1E[XW] +2b_2E[W^2] -2E[YW]
\end{align*}
$$

偏微分が $0$ になるとき

$$
\begin{align*}
  &\left\{
    \begin{array}{l}
      b_1E[X^2] + b_2E[XW] - E[XY] = 0 \\
      b_1E[XW] + b_2E[W^2] - E[YW] = 0
    \end{array}
  \right.
\\ &\Leftrightarrow \\
  &\left\{
    \begin{array}{l}
      b_1 + 0.9b_2 - 0.72 = 0 \\
      0.9b_1 + b_2 - 0.8 = 0
    \end{array}
  \right.
\\ &\Leftrightarrow \\
&b_1 = 0, b_2 = 0.8
\end{align*}
$$

## [4]

### [4-1]
条件より
$$
\begin{align*}
r_{X_AY_A} = \frac{Cov(X_A, Y_A)}{\sqrt{V[X_A]V[Y_A]}} = Cov(X_A, Y_A) = E[X_AY_A] - E[X_A]E[Y_A] = 0\\
\end{align*}
$$

$X_A$, $T_A$ の相関係数
$$
\begin{align*}
r_{X_AT_A} &= \frac{Cov(X_A, T_A)}{\sqrt{V[X_A]V[T_A]}}
&= \frac{Cov(X_A, T_A)}{\sqrt{V[T_A]}}
\end{align*}
$$

分母
$$
\begin{align*}
V[T_A] &= V[X_A + Y_A]\\
&= V[X_A] + V[Y_A] + 2Cov(X_A, Y_A)\\
&= 1 + 1 + 0\\
&= 2
\end{align*}
$$
分子
$$
\begin{align*}
Cov(X_A, T_A) &= E[X_AT_A] - E[X_A]E[T_A]\\
&= E[X_A(X_A + Y_A)] - E[X_A]E[X_A + Y_A]\\
&= E[X_A^2] + E[X_AY_A] - E[X_A]^2 - E[X_A]E[Y_A]\\
&= V[X_A] + E[X_AY_A] - E[X_A]E[Y_A]\\
&= 1
\end{align*}
$$

したがって,

$$
\begin{align*}
r_{X_AT_A} &= \frac{Cov(X_A, T_A)}{\sqrt{V[T_A]}}
&= \frac{1}{\sqrt{2}}
\end{align*}
$$

$X_A$ と $Y_A$ を入れ替えても同様なので、$r_{Y_AT_A} = \frac{1}{\sqrt{2}}$

### [4-2]

$$
\begin{align*}
r_{X_AY_A/T_A} &= \frac{r_{X_AY_A} - r_{X_AT_A}r_{Y_AT_A}}{\sqrt{(1-r_{X_AT_A}^2)(1-r_{Y_AT_A}^2)}}\\
&= \frac{0 - 1/2}{\sqrt{(1 - 1/2)(1-1/2)}}\\
&= -2
\end{align*}
$$

$T_A$ で条件付けたときの $X_A$ と $Y_A$ には負の相関があり、これをセレクションバイアスという