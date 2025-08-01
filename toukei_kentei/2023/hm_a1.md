## [1]
A, Bさんの標準偏差
$$
\begin{align*}
S_A &= \left(\frac{74 - 70}{4} \times 10 \right) +50 = 60\\
S_B &= \left(\frac{86 - 79}{4} \times 10 \right) +50 = 67.5
\end{align*}
$$

文系学生の点数分布は70を中心とした正規分布なので、合格率50%  
理系学生の点数分布を標準化した場合の70点相当は、
$$
z=\frac{70-79}{4} = -2.25
$$
標準正規分布表から 
$$
Q(-2.25) = 1-Q(2.25) = 1 - 0.0122 = 0.9878
$$
全体の合格率は、文理の重み和から  
$$
50 * \frac{2}{3} + 98.78 * \frac{1}{3} = 66.26 [\%]
$$

## [2]

$$
\begin{align*}
E[X] &= \sum_{i=1}^n p_i E[X_i]\\
&= \frac{2}{3} * 70 + \frac{1}{3} * 79\\
&= 73
\\\\
V[X] &= \left(\frac{2}{3} * 4^2 + \frac{1}{3} *  4^2\right) 
+ \left(\frac{2}{3}\cdot\frac{1}{3}\cdot(70^2) + \frac{2}{3}\cdot\frac{1}{3}\cdot(79^2)\right) 
- 2 * \frac{2}{3}\cdot\frac{1}{3}\cdot 70\cdot 79\\
&= 34
\end{align*}
$$

$$
\begin{align*}
S_A' &= \left(\frac{74 - 73}{\sqrt{34}} \times 10 \right) +50 = 51.7\\
S_B' &= \left(\frac{86 - 73}{\sqrt{34}} \times 10 \right) +50 = 72.3
\end{align*}
$$

## [3]
### [3-1]

### [3-2]
正規分布 $N(0, 1)$の確率密度関数の微分
$$
\begin{align*}

\frac{df(x)}{dx} &= \frac{d}{dx} \frac{1}{\sqrt{2\pi\sigma^2}}\exp{\left[-\frac{(x-\mu)^2}{2\sigma^2}\right]}\\
&= \frac{1}{\sqrt{2\pi\sigma^2}}\cdot -\frac{x-\mu}{\sigma^2}\exp{\left[-\frac{(x-\mu)^2}{2\sigma^2}\right]}
\end{align*}
$$
混合分布の確率密度関数の微分
$$
\begin{align*}
f(x) &= \frac{2}{3} f_文(x) + \frac{1}{3} f_理(x)\\
\\
\frac{df(x)}{dx} &= \frac{2}{3} \frac{df_文(x)}{dx} + \frac{1}{3} \frac{df_理(x)}{dx}\\
&= \frac{1}{\sqrt{2\pi\sigma^2}\sigma^2}\left\{-\frac{2(x-70)}{3}\exp{\left[-\frac{(x-70)^2}{2\sigma^2}\right]}-\frac{(x-79)}{3}\exp{\left[-\frac{(x-79)^2}{2\sigma^2}\right]}\right\}
\\
\end{align*}
$$
$x\le70$ のとき、$f'(x)\gt0$, $x\ge79$のとき、$f'(x)\lt0$  
$70\lt x\lt79$ の範囲に $f'(x)=0$ となる最頻値が存在する



## [補足]
### 混合分布の確率密度関数  
確率密度関数 $f_i$ の混合比を$p_i$ ($\sum_{i=1}^n p_i = 1$)としたとき、
$$
f(x) = \sum_{i=1}^n p_i f_i(x)
$$
### f(x)の積分が1になることの確認
$f_i(x)$の定義域を ($x \in \mathcal{X} $) とする
$$
\begin{align*}
\int_{\mathcal{X}}f(x)dx &= \int_{\mathcal{X}}\sum_{i=1}^n p_i f_i(x)dx\\
&= \int_{\mathcal{X}} (p_1f_1(x) + \cdots + p_nf_n(x)) dx\\
&= \int_{\mathcal{X}}p_1f_1(x)dx + \cdots + \int_{\mathcal{X}}p_nf_n(x) dx\\
&= \sum_{i=1}^n \int_{\mathcal{X}}p_i f_i(x)dx\\
&= \sum_{i=1}^n p_i\int_{\mathcal{X}} f_i(x)dx\\
&= \sum_{i=1}^n p_i\\
&= 1
\end{align*}
$$

### 混合分布の期待値と分散
期待値
$$
\begin{align*}
E[X] &= \int_{\mathcal{X}} x \sum_{i=1}^n p_i f_i(x) dx\\
&= \sum_{i=1}^n p_i \int_{\mathcal{X}} x   f_i(x) dx\\
&= \sum_{i=1}^n p_i E[X_i]
\end{align*}
$$

分散
$$
\begin{align*}
E[X^2] &= \int_{\mathcal{X}} x^2 \sum_{i=1}^n p_i f_i(x) dx\\
&= \sum_{i=1}^n p_i \int_{\mathcal{X}} x^2   f_i(x) dx\\
&= \sum_{i=1}^n p_i E[X_i^2]
\\
\\
V[X] &= E[X^2] - (E[X])^2\\
&= \sum_{i=1}^n p_i E[X_i^2] - \left( \sum_{i=1}^n p_i E[X_i] \right)^2\\
&= \sum_{i=1}^n p_i E[X_i^2] - \left( \sum_{i=1}^n  p_i^2E[X_i]^2 + \sum_{i\neq j}^n p_ip_jE[X_i]E[X_j] \right)\\
&= \sum_{i=1}^n p_i \left(V[X_i] + E[X_i]^2\right) - \left( \sum_{i=1}^n  p_i^2E[X_i]^2 + \sum_{i\neq j}^n p_ip_jE[X_i]E[X_j] \right)\\
&= \sum_{i=1}^n p_i V[X_i] +  \sum_{i=1}^n  \left(p_i E[X_i]^2 -  p_i^2E[X_i]^2 \right) - \sum_{i\neq j}^n p_ip_jE[X_i]E[X_j]\\
&= \sum_{i=1}^n p_i V[X_i] +  \sum_{i=1}^n  (1 - p_i)p_i E[X_i]^2  - \sum_{i\neq j}^n p_ip_jE[X_i]E[X_j]
\end{align*}
$$
