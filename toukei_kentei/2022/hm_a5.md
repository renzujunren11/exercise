## [1]
$$
\begin{align*}
\sigma_{XY} &= \rho_{XY}\sigma_X\sigma_Y\\
E[D] &= E[Y-X]\\
&= 120 - 120 \\
&= 0\\
\\
V[D] &= V[Y-X]\\
&= V[X] + V[Y] - 2\sigma_{XY}\\
&= 12^2 + 12^2 - 2\cdot0.75\cdot12^2\\
&= 72
\end{align*}
$$
正規分布の再生性より$D$ は 期待値$0$, 分散$77$ の正規分布に従う
$$
\begin{align*}
P(D\le-4) &= P\left(Z\le\frac{-4}{\sqrt{72}}\right)
&= P\left(Z\le-\right)\\
&\fallingdotseq0.3192
\end{align*}
$$

## [2]
$$
\begin{align*}
E[Y|X=132] &= \alpha + \beta x\\
&= (\mu_Y -\beta\mu_X) + \beta x\\
&= \mu_Y + \frac{\sigma_{XY}}{\sigma_X^2}(x-\mu_X)\\
&= 120 + \frac{0.75\cdot12^2}{12^2}(132-120)\\
&= 129\\
\\
V[Y|X = 132] &= \sigma^2\\
&= \sigma_Y^2 - \frac{\sigma_{XY}^2}{\sigma_X^2}\\
&= 12^2 - \frac{(0.75\cdot12^2)^2}{12^2}\\
&= 63
\end{align*}
$$

1回目の測定値が132mmHGで条件付けた時の2回目の測定値の期待値は129mmHGであり、母平均に近づいている  
132-129=3[mmHG]は平均への回帰で説明される

## [3]

$$
\begin{align*}
V[X] &= V[\theta + \epsilon_1]\\
&= V[\theta] + V[\epsilon_1] + 2Cov(\theta, \epsilon_1)\\
&= \gamma^2 + \psi^2\\
V[Y] &= \gamma^2 + \psi^2\\
\\
V[X+Y] &= V[X] + V[Y] + 2Cov(X, Y)\\
V[X+Y] &= V[2\theta + \epsilon_1 + \epsilon_2]\\
&= 4V[\theta] + V[\epsilon_1] + V[\epsilon_2]\\
&= 4\gamma^2 + 2\psi^2\\
Cov(X, Y) &= 1/2(V[X+Y] - V[X] - V[Y])\\
&= 1/2(4\gamma^2 + 2\psi^2 - 2(\gamma^2 + \psi^2))\\
&= \gamma^2\\
\\
\gamma^2 &= 0.75\cdot12^2\\
&=108\\
\psi^2 &= V[X] - \gamma^2\\
&= 12^2 - 0.75\cdot12^2\\
&= 36
\end{align*}
$$

## [4]

$$
\begin{align*}
Cov(\theta, X) &= Cov(\theta, \theta+\epsilon_1)\\
&= E[\theta(\theta+\epsilon_1)] - E[\theta]E[\theta+\epsilon_1]\\
&= E[\theta^2] + E[\theta\epsilon_1] - (E[\theta]^2 + E[\theta]E[\epsilon_1])\\
&= V[\theta] + (Cov(\theta, \epsilon_1) + E[\theta]E[\epsilon_1]) - E[\theta]E[\epsilon_1]\\
&= \gamma^2
\\
E[\theta|X] &= E[\theta] + \frac{Cov(\theta, X)}{V[X]}(x-E[X])\\
&= \mu + \frac{\gamma^2}{\gamma^2 + \psi^2}(x-\mu)\\
&= 120 + \frac{108}{108+36}(132-120)\\
&= 129\\
\\
V[\theta|X] &= V[\theta] - \frac{Cov(\theta, X)^2}{V[X]}\\
&= \gamma^2 - \frac{\gamma^4}{\gamma^2 + \psi^2}\\
&= \frac{\gamma^2\psi^2}{\gamma^2 + \psi^2}\\
&= \frac{108\cdot36}{108+36}\\
&= 27
\end{align*}
$$

## [5]
$$
\begin{align*}
E[Y|X] &= E[\theta+\epsilon_2|X]
\end{align*}
$$