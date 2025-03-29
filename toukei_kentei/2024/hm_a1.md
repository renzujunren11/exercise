## [1-1]
$$
R_2 = \begin{bmatrix}1.00&0.32\\0.32&1.00\end{bmatrix}
$$
固有値、固有ベクトルを求める

$$\begin{align*}
\bold{A}\boldsymbol{x} &= \lambda \boldsymbol{x}\\
\begin{bmatrix}1.00&0.32\\0.32&1.00\end{bmatrix} \begin{bmatrix}x_1\\x_2\end{bmatrix} &= \lambda \begin{bmatrix}x_1\\x_2\end{bmatrix}\\
\begin{bmatrix}x_1 + 0.32x_2\\0.32x_1 +x_2\end{bmatrix} &=  \begin{bmatrix}\lambda x_1\\ \lambda x_2\end{bmatrix}\\
\begin{bmatrix}(1-\lambda)x_1 + 0.32x_2\\0.32x_1 +(1-\lambda)x_2\end{bmatrix} &=  \begin{bmatrix}0\\ 0\end{bmatrix}\\
\end{align*}$$
$\lambda_1 = 1.32$, $\lambda_2 = 0.68$  
$\boldsymbol{a} = \begin{bmatrix}1/\sqrt{2}\\ 1/\sqrt{2}\end{bmatrix}$, $\boldsymbol{b} = \begin{bmatrix}1/\sqrt{2}\\ -1/\sqrt{2}\end{bmatrix}$

## [1-2]
$$
c_1 = \frac{\lambda_1}{\lambda_1 + \lambda_2} = \frac{1.32}{1.32 + 0.68} = 0.66\\
c_2 = \frac{\lambda_2}{\lambda_1 + \lambda_2} = \frac{0.68}{1.32 + 0.68} = 0.34
$$

$$
\rho_{1, 1} = \frac{\sqrt{\lambda_1}a_{1, 1}}{r_1} = \frac{\sqrt{1.32} \cdot 1/\sqrt{2}}{1} = 0.812
$$

## [2-1]
$$
c_1 = \frac{3.67}{3.67 + 1.24 + 0.05} = 0.74\\
c_2 = \frac{1.24}{3.67 + 1.24 + 0.05} = 0.25
c_1 + c_2 = 0.99
$$

第一主成分は総合力、第二主成分は理系能力

## [2-2]
5変量正規分布のパラメータ$(\boldsymbol{\mu}, \boldsymbol{\Sigma})$が  
$\boldsymbol{\mu} = (0, 0, 0, 0, 0)$、  $\boldsymbol{\Sigma} = 
\begin{bmatrix}
1.00 & 0.95 & 0.89 & 0.32 & 0.35\\ 
0.95 & 1.00 & 0.94 & 0.41 & 0.47\\ 
0.89 & 0.94 & 1.00 & 0.64 & 0.66\\ 
0.32 & 0.41 & 0.64 & 1.00 & 0.98\\ 
0.35 & 0.47 & 0.66 & 0.98 & 1.00\\ 
\end{bmatrix}$  
のとき、  
$$
z_1 = \boldsymbol{a}^T\boldsymbol{x} = -0.44x_1 -0.47x_2 -0.51x_3 - 0.40x_4 - 0.41x_5
$$  
の期待値と分散は、
$$
E[z_1] = \boldsymbol{a}^T\boldsymbol{\mu} = 0
$$
$$
V[z_1] = \boldsymbol{a}^T\boldsymbol{\Sigma}\boldsymbol{a} = 3.678
$$
$z_1$の上側80％点は
$$
z_{1, \alpha=0.8} = E[z_1] + 0.84 * \sqrt{V[z_1]} = 1.61
$$
第1主成分と合計得点の相関係数は、
$$

$$

## [3]
$$
z_1 = -0.44*1.22 -0.47*1.33 -0.51*1.58 - 0.40*1.44 - 0.41 * 1.28 = -3.07\\
z_2 = -0.46*1.22 -0.37*1.33 -0.15*1.58 + 0.58*1.44 + 0.54 * 1.28 = 0.236
$$