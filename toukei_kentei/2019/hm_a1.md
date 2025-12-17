## [1]
偏差値 → 得点
$$
\begin{align*}
\frac{X-100}{20} \cdot 10 + 50 &= 54\\
\because X = 108
\end{align*}
$$
標準化した得点は、$0.4$  
標準正規分布で $P(z\ge 0.4) = 0.3446$ なので、上位 $34\%$  
合格者のうち、$0.3446 / 0.5 = 0.6892$ なので、上位 $69\%$  
入学者のうち、$(0.3446-0.1) / 0.4 = 0.6115$ なので、上位 $61\%$

## [2]
最低点は全体の中央値。受験者の得点は正規分布なので、中央値は平均に等しい。  
最高点は受験者での上位10%の得点なので、標準正規分布表より上側確率が0.10となるのは、$z=1.28$  
$$
\begin{align*}
\frac{X-100}{20}&= 1.28\\
\because X &= 125.6
\end{align*}
$$
よって、入学者の最低点は$100$, 最高点は$125.6$

## [3]
受験者全体の得点分布
$$
\begin{align*}
f &= \frac{1}{\sqrt{2\pi\cdot20^2}}\exp\left[-\frac{(z-100)^2}{2\cdot20^2}\right]\\
&=\frac{1}{20\sqrt{2\pi}}\exp\left[-\frac{(z-100)^2}{2\cdot20^2}\right]\\
\end{align*}
$$
合格者の得点分布は、平均よりも上側の部分になるので  
確率密度関数に2をかけて
$$
\begin{align*}
2\cdot\frac{1}{20\sqrt{2\pi}}\exp\left[-\frac{(z-100)^2}{2\cdot20^2}\right]dz &= \frac{1}{10}\cdot\frac{1}{\sqrt{2\pi}}\exp\left[-\frac{(\frac{z-100}{20})^2}{2}\right]\\
&= \frac{1}{10}\varphi\left(\frac{z-100}{20}\right) \quad (z\ge 100)
\end{align*}
$$

## [4]