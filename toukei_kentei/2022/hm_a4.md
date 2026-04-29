## [1]
信頼性は、測定結果のばらつきが小さいこと  
妥当性は、測定結果の期待値が真の値に近いこと  
校正のズレた重量計は、測定値のばらつきが小さくても、本当の重さからは常に一定のズレがある

[模範回答]  
妥当性とは、測定すべきことを測定しているかどうか
信頼性は、測定結果の安定性及び一貫性  
数学の能力を測りたいときに、計算問題ばかりを出題することは、真に測りたい数学の能力を測れていない

## [2]
$$
\begin{align*}
s_T^2 &= V[T]\\
&= V[X_1 + X_2 + \cdot + X_m]\\
&= \sum_{i=1}^mV[X_i] + 2\sum_{j\lt k}^mCov(X_j, X_k)\\
&= \sum_{i=1}^ms_i^2 + 2\sum_{j\lt k}^ms_{jk}\\
&= m\bar{V} + m(m-1)\bar{C}\\
\\

\alpha &= \frac{m}{m-1}\left(1-\frac{\sum_{j=1}^ms_j^2}{s_T^2}\right)\\
&= \frac{m}{m-1}\left(1-\frac{m\bar{V}}{m\bar{V} + m(m-1)\bar{C}}\right)\\
&= \frac{m}{m-1}\left(\frac{(m-1)\bar{C}}{\bar{V} + (m-1)\bar{C}}\right)\\
&= \frac{m\bar{C}}{\bar{V} + (m-1)\bar{C}}\\
\\
s_W^2 &= V[W]\\
&= V[Z_1 + Z_2 + \cdots + Z_m]\\
&= \sum_{i=1}^mV[Z_i] + 2\sum_{j\lt k}^mCov(Z_j, Z_k)\\
&= m + 2\sum_{j\lt k}^mr_{jk}\\
&= m + m(m-1)\bar{R}\\
\\

\alpha' &= \frac{m}{m-1}\left(1-\frac{m}{s_W^2}\right)\\
&= \frac{m}{m-1}\left(1-\frac{m}{m + m(m-1)\bar{R}}\right)\\
&= \frac{m}{m-1}\left(\frac{(m-1)\bar{R}}{1 + (m-1)\bar{R}}\right)\\
&= \frac{m\bar{R}}{1 + (m-1)\bar{R}}\\
\\
\end{align*}
$$

## [3]
$$
\begin{align*}
\alpha'&\ge0.8\\
\frac{m\cdot0.5}{1 + (m-1)\cdot0.5}&\ge 0.8\\
m&\ge 4
\end{align*}
$$

## [4]
### [4-1]
