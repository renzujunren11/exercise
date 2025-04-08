## [1-1]

$$\begin{align*}
P &= - \frac{1}{2}Q_nDQ_n\\
&= - \frac{1}{2}\frac{1}{3}\frac{1}{3}
\begin{pmatrix}2 & -1 & -1\\-1 & 2 &-1\\-1 & -1 & 2\end{pmatrix}
\begin{pmatrix}0 & 4 & 2\\4 & 0 &2\\2 & 2 & 0\end{pmatrix}
\begin{pmatrix}2 & -1 & -1\\-1 & 2 &-1\\-1 & -1 & 2\end{pmatrix}\\
&= - \frac{1}{18}
\begin{pmatrix}-6 & 6 & 2\\6 & -6 &2\\0 & 0 & -4\end{pmatrix}
\begin{pmatrix}2 & -1 & -1\\-1 & 2 &-1\\-1 & -1 & 2\end{pmatrix}\\
&= - \frac{1}{18}
\begin{pmatrix}-20 & 16 & 4\\16 & -20 &4\\4 & 4 & -8\end{pmatrix}\\
&= - \frac{2}{9}
\begin{pmatrix}-5 & 4 & 1\\4 & -5 &1\\1 & 1 & -2\end{pmatrix}
\end{align*}$$

## [1-2]
$$\begin{align*}
\tilde{X} &= U_2\Delta_2^{1/2}\\
&= \begin{pmatrix}1/\sqrt{2} & 1/\sqrt{6} \\-1/\sqrt{2} & 1/\sqrt{6} \\0 & -2/\sqrt{6}\end{pmatrix}\begin{pmatrix}\sqrt{2} & 0 \\0 & 2/\sqrt{6}\end{pmatrix}\\
&= \begin{pmatrix}1 & 1/3\\-1 & 1/3 \\ 0 & -2 / 3\end{pmatrix}\\
\end{align*}$$

## [2]
$\mathrm{x}_{i} = (x_{i1}, x_{i2}, x_{i3})$ 、$X = \begin{pmatrix}x_{11} & x_{12} & x_{13}\\x_{21} & x_{22} & x_{23}\\x_{31} & x_{32} & x_{33}\end{pmatrix}$として、
$XX^T$ を計算してすると

$$\begin{align*}
XX^T &= \begin{pmatrix}x_{11} & x_{12} & x_{13}\\x_{21} & x_{22} & x_{23}\\x_{31} & x_{32} & x_{33}\end{pmatrix}\begin{pmatrix}x_{11} & x_{21} & x_{31}\\x_{12} & x_{22} & x_{32}\\x_{13} & x_{23} & x_{33}\end{pmatrix}\\
&= \begin{pmatrix}|\mathrm{x}_{1}|^2 & \mathrm{x}_{1}\cdot \mathrm{x}_{2} & \mathrm{x}_{1}\cdot \mathrm{x}_{3}\\\mathrm{x}_{1}\cdot \mathrm{x}_{2} & |\mathrm{x}_{2}|^2 & \mathrm{x}_{2}\cdot \mathrm{x}_{3}\\\mathrm{x}_{1}\cdot \mathrm{x}_{3} & \mathrm{x}_{2}\cdot x_{3} & |\mathrm{x}_{3}|^2\end{pmatrix}
\end{align*}$$

また、$\mathrm{x}_{i}$と$\mathrm{x}_{j}$とのユークリッド距離の二乗は、
$$\begin{align*}
d_{ij}^2 &= (x_{i1}-x_{j1})^2 + (x_{i2}-x_{j2})^2 + (x_{i3}-x_{j3})^2\\
&= x_{i1}^2 + x_{i2}^2 + x_{i3}^2\\
&\quad + x_{j1}^2 + x_{j2}^2 + x_{j3}^2\\
&\quad +-2(x_{i1}x_{j1} + x_{i2}x_{j2} + x_{i3}x_{j3})\\
&= |\mathrm{x}_{i}|^2 + |\mathrm{x}_{j}|^2 - 2\mathrm{x}_{i}\cdot \mathrm{x}_{j}
\end{align*}$$

$D$は、
$$\begin{align*}
D &= \begin{pmatrix}
0 
& |\mathrm{x}_{1}|^2 + |\mathrm{x}_{2}|^2 - 2\mathrm{x}_{1}\cdot \mathrm{x}_{2} 
& |\mathrm{x}_{1}|^2 + |\mathrm{x}_{3}|^2 - 2\mathrm{x}_{1}\cdot \mathrm{x}_{3}\\
|\mathrm{x}_{2}|^2 + |\mathrm{x}_{1}|^2 - 2\mathrm{x}_{2}\cdot \mathrm{x}_{1} 
& 0
& |\mathrm{x}_{2}|^2 + |\mathrm{x}_{3}|^2 - 2\mathrm{x}_{2}\cdot \mathrm{x}_{3}\\
|\mathrm{x}_{3}|^2 + |\mathrm{x}_{1}|^2 - 2\mathrm{x}_{3}\cdot \mathrm{x}_{1} 
& |\mathrm{x}_{3}|^2 + |\mathrm{x}_{2}|^2 - 2\mathrm{x}_{3}\cdot \mathrm{x}_{2} 
& 0
\end{pmatrix}\\
&= diag(XX^T)\mathbf{1}_3\mathbf{1}_3^T + \mathbf{1}_3\mathbf{1}_3^Tdiag(XX^T) - 2XX^T
\end{align*}$$
