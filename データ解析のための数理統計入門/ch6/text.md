
## 大数の法則

独立同分布に従う確率変数Xが平均 $\mu$, 分散 $\sigma^2$ をもつとき  
標本平均 $\bar{X_n} = \frac{1}{n}\sum_{i=1}^n X_i$ は $n \rightarrow \infty$で

$$
P(|\bar{X}_n - \mu| \gt c) \rightarrow 0
$$

「標本平均が母平均に収束する」

[ 証明 ]  
確率変数$\bar{X}_n$の平均は$\mu$, 分散は$\sigma^2/n$である。  
チェビシェフの不等式より
$$
P(|\bar{X}_n-\mu|\ge c) \le \frac{E[(\bar{X}_n-\mu)^2]}{c^2}
$$
ここで、$E[(\bar{X}_n-\mu)^2] = Var(\bar{X}_n) = \sigma^2/n$であることに注意すると  
$$
\frac{E[(\bar{X}_n-\mu)^2]}{c^2} = \frac{\sigma^2}{nc^2}
$$
したがって、
$$
P(|\bar{X}_n-\mu|\ge c) \le \frac{\sigma^2}{nc^2}
$$
上式の右辺は、$n\rightarrow0$より、$P(|\bar{X}_n-\mu|\ge c)\rightarrow0$

<details>
  <summary>チェビシェフの不等式
  </summary>

  確率変数Xの平均を $\mu$ とすると、任意の正の実数cに対して次の不等式が成り立つ

  $$
  P(|X-\mu|\ge c) \le \frac{E[(X-\mu)^2]}{c^2}
  $$
</details>

## 中心極限定理

独立同分布に従う確率変数$X_1, \dots, X_n$について、$E[X_i]=\mu$, $Var(X_i)=\sigma^2$とする。  
$X_i$の積率母関数が存在するとき、
$$
\lim_{n \rightarrow 0} P(\sqrt{n}(\bar{X} - \mu)/\sigma \le x) = \int_{\infty}^x \frac{1}{\sqrt{2\pi}}e^{-\mu^2/2}du = \Phi(x)
$$

「$Z=\frac{\bar{X} - \mu}{\sqrt{\sigma^2/n}}$とおいた場合、Zの分布関数$F(z) = P(Z\le z)$が標準正規分布の分布関数に収束する(分布収束)」

[証明]
$Z_i = \frac{X_i-\mu}{\sigma}$とおくと、$E[Z_i] = 0$, $Var(Z_i) = 1$, $E[bar{Z}] = 0$, $Var(bar{Z}) = 1/n$となる。  

$\sqrt{n}\bar{Z} = \frac{\sqrt{n}}{n} \sum Z_i= Z_1/\sqrt{n} + \cdots + Z_n/\sqrt{n}$より、この積率母関数は次のように書ける。  
$$\begin{align*}
M_{\sqrt{n}\bar{Z}}(t) &= E[\exp(t(Z_1/\sqrt{n} + \cdots + Z_n/\sqrt{n}))]\\
&=E[\exp(t / \sqrt{n}(Z_1 + \cdots + Z_n))]\\
&=E[\exp(t Z_1/ \sqrt{n})\cdots\exp(t Z_n/ \sqrt{n})]\\
&=\left(E[\exp(t Z_1/ \sqrt{n})]\right)^n
\end{align*}$$

$Z_1$の積率母関数を$\varphi(\theta) = E[e^{\theta Z_1}]$とおくと、$E[exp(tZ_1/\sqrt{n})] = \varphi(t/\sqrt{n})$なので、$\varphi(\cdot)$をマクローリン展開すると、
$$
\varphi(\frac{t}{\sqrt{n}}) = \varphi(0) + \frac{t}{\sqrt{n}}\varphi'(0) + \frac{t^2}{2n}\varphi''(0) + o(\frac{1}{n})
$$
ここで、$\varphi(0) = 1$, $\varphi'(0) = E[Z_1] = 0$, $\varphi''(0) = E[Z_1^2] = Var(Z_1) = 1$より、
$$
\varphi(\frac{t}{\sqrt{n}}) = 1 + \frac{t^2}{2n} + o(\frac{1}{n})
$$
したがって、
$$\begin{align*}
M_{\sqrt{n}\bar{Z}}(t) &= \left(1 + \frac{t^2}{2n} + o(\frac{1}{n})\right)^n\\
&= \left(1 + \frac{\frac{t^2}{2} + o(1)}{n})\right)^n\\
&\rightarrow e^{t^2/2}
\end{align*}$$

## 経験分布関数の真の累積分布関数に対する不偏性の証明
確率変数 $X_1, \dots, X_n$ が独立に同一の分布 $F(x)$ からの標本とする  
経験分布関数は次のように定義される
$$
\hat{F}_n(x) = \frac{1}{n}\sum_{i=1}^n I(X_i \le x)
$$
ここで、$I(X_i \le x)$は指示関数  
各指示関数の期待値は、
$$
E[I(X_i \le x)] = P(X_i \le x) = F(x)
$$
$\hat{F}_n(x)$ の期待値は、
$$\begin{align*}
E[\hat{F}_n(x)] &= E\left[\frac{1}{n}\sum_{i=1}^n I(X_i \le x)\right]\\
&= \frac{1}{n}\sum_{i=1}^n E[I(X_i \le x)]\\
&= \frac{1}{n}\sum_{i=1}^n F(x)\\
&= F(x).
\end{align*}$$
