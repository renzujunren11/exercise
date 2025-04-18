## ア
期待値の線形性より, $E[X+Y] = E[X] + E[Y]$  
よって、E[X + Y] = 50 + 50 = 100

## イ
$V[X + Y] = V[X] + V[Y] + 2Cov(X, Y) = 100 + 100 + 120 = 320$

# ウ
正規分布に従う変数の和は正規分布に従うのでX+Yも正規分布に従う  
120点が正規分布の何%点かを調べる  
$\frac{120 - 100}{\sqrt{320}} = \frac{\sqrt{5}}{2} = \frac{2.236}{2} \fallingdotseq 1.108$  
標準正規分布表で1.12となる確率は0.1314. よって13.1(%)

## エ
標準正規分布表で確率が0.2に最も近いのは、0.84  
$\frac{a-100}{\sqrt{320}} = 0.84$. よってa=115

## オ、カ
YのXの条件付き分布も正規分布に従う  
このとき、条件付き分布の期待値と分散は以下のように求められる
相関係数は, $\rho = \frac{60}{10*10} = 0.6$  
Xの条件付き分布の期待値と分散は,
$$\begin{align*}
\mu_{Y|X} &= \mu_Y + \rho\frac{\sigma_y}{\sigma_x}(X-\mu_X) = 50 + 0.6*\frac{10}{10}(50-50) = 50\\
\sigma_{Y|X}^2 &= \sigma_Y^2(1-\rho^2) = 10^2(1-0.6^2) = 64
\end{align*}$$

## キ
$P(X+Y\ge120|X=50) = P(Y\ge70|X=50)$なので、70点が正規分布の何%点かを調べる  
$\frac{70 - 50}{\sqrt{64}} =  0.25$
標準正規分布表で0.25となる確率は0.4013. よって40.1(%)
