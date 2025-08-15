表から計算できる値の整理
$$
\begin{align*}
\bar{x} &= \frac{1}{45}\sum_{i=1}^{45}x_i\\
\bar{y} &= \frac{1}{45}\sum_{i=1}^{45}y_i\\
s_x^2 &= \frac{1}{45}\sum_{i=1}^{45}(x_i - \bar{x})^2 = \frac{1}{45}\sum_{i=1}^{45}x_i^2 - \bar{x}^2\\
s_y^2 &= \frac{1}{45}\sum_{i=1}^{45}(y_i - \bar{y})^2 = \frac{1}{45}\sum_{i=1}^{45}y_i^2 - \bar{y}^2\\
\rho_{xy} &= \frac{Cov(x, y)}{\sqrt{s_x^2s_y^2}}\\
Cov(x, y) &= \frac{1}{45}\sum_{i=1}^{45}(x_i - \bar{x})(y_i - \bar{y})\\
&= \frac{1}{45}\sum_{i=1}^{45}(x_iy_i -\bar{y}x_i - \bar{x}y_i + \bar{x}\bar{y})\\
&= \frac{1}{45}\sum_{i=1}^{45}x_iy_i - \bar{x}\bar{y}\\
&= \rho_{xy}\sqrt{s_x^2s_y^2}
\\
\sum_{i=1}^{45}x_i &= 45\cdot8.6 = 387\\
\sum_{i=1}^{45}y_i &= 45\cdot4.9 = 220.5\\
\sum_{i=1}^{45}x_i^2 &= 45(2.0 + 8.6^2) = 3418.2\\
\sum_{i=1}^{45}y_i^2 &= 45(2.0 + 4.9^2) = 1170.45\\
\sum_{i=1}^{45}x_iy_i &= 45(0.16\sqrt{2.0\cdot2.0} + 8.6\cdot4.9) = 1910.7
\end{align*}
$$

## [1]
各試合の得点を$z$とおく
$$
\begin{align*}
\bar{z} &= \frac{1}{90} \left(\sum_{i=1}^{45}x_i + \sum_{i=1}^{45}y_i\right)\\
&= \frac{1}{90} (387+220.5)\\
&= 6.75\\
\\
s_z^2 &= \frac{1}{90} \left(\sum_{i=1}^{45}(x_i - \bar{z})^2 + \sum_{i=1}^{45}(y_i - \bar{z})^2\right)\\
&= \frac{1}{90}\sum_{i=1}^{45}(x_i^2+ y_i^2 - 2\bar{z}(x_i+y_i) + 2\bar{z}^2)\\
&= \frac{1}{90}(3418.2 + 1170.45 -2\cdot6.75(387+220.5) + 45\cdot2\cdot6.75^2)\\
&= 5.4225
\end{align*}
$$

## [2]
$$
\begin{align*}
\bar{w} &= \frac{1}{45}\sum_{i=1}^{45}(x_i + y_i)\\
&= \bar{x} + \bar{y}\\
&=13.5\\
\\
\bar{d} &= \frac{1}{45}\sum_{i=1}^{45}(x_i - y_i)\\
&= \bar{x} - \bar{y}\\
&= 3.7\\
\\
s_w^2 &= \frac{1}{45}\sum_{i=1}^{45}(w_i - \bar{w})^2\\
&= \frac{1}{45}\sum_{i=1}^{45}(x_i^2 + y_i^2 + 2x_iy_i - 2\bar{w}(x_i+y_i) + \bar{w}^2)\\
&= \frac{1}{45}(3418.2 +1170.45 + 2\cdot1910.7 - 2\cdot13.5\cdot(387 + 220.5) + 45\cdot13.5^2)\\
&= 4.64\\
\\
s_d^2 &= \frac{1}{45}\sum_{i=1}^{45}(d_i - \bar{d})^2\\
&= \frac{1}{45}\sum_{i=1}^{45}(x_i^2 + y_i^2 - 2x_iy_i - 2\bar{d}(x_i-y_i) + \bar{d}^2)\\
&= \frac{1}{45}(3418.2 +1170.45 - 2\cdot1910.7 - 2\cdot3.7\cdot(387 - 220.5) + 45\cdot3.7^2)\\
&= 3.36
\end{align*}
$$

## [3]

$$
\begin{align*}
Cov(w, d) &= \frac{1}{45}\sum_{i=1}^{45}(w_i-\bar{w})(d_i-\bar{d})\\
&= \frac{1}{45}\sum_{i=1}^{45}w_id_i -\bar{w}\bar{d}\\
&= \frac{1}{45}\sum_{i=1}^{45}(x^2 - y^2) -\bar{w}\bar{d}\\
&= \frac{1}{45}(3418.2 - 1170.45) - 13.5\cdot3.7\\
&= 0\\
\rho_{wd} &= 0
\end{align*}
$$

## [4]
$$
\begin{align*}
E[U-V] &= E[U] - E[V]\\
&= 7.1 - 7.4 \\
&= -0.3\\
\\
V[U-V] &= V[U] + V[V] - 2Cov(U, V)\\
&= 6.1 + 1.4 - 0\\
&= 7.5
\end{align*}
$$
正規分布の再生性より、$U-V$ は　正規分布 $N(-0.3, 7.5)$ に従う  
$U-V$ を標準化し $Z_{U-V}$ とおくと  
$U-V\ge0$ すなわち $Z_{U-V} \ge \frac{0 - (-0.3)}{\sqrt{7.5}} = 0.1095...$ となる確率は、  
標準正規分布表より、およそ $0.4562$
