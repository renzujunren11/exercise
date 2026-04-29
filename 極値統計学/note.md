### 極値データ
$n$ を定数として、独立に同一の分布に従う確率変数列
$$
X_1, X_2 \dots, X_n
$$
を考える。

$X$ の分布は
$$
F(x) = P(X_i \le x) \quad(i=1, 2, \dots, n)
$$
とする。
ここで、順序統計量を 
$$
X_{(1)} \le X_{(2)} \le \dots \le X_{(n)}
$$
とする。

極値統計量を
$$
Z_n := X_{(n)} = \max{\{X_1, X_2 \dots, X_n\}}
$$
とする。  

このとき、$n$ が十分大きいときの $Z_n$ の分布を知りたい。  
また、上位 $r \ (\gt 1)$ 個の順序統計量
$$
(X_{(n)}, X_{(n-1)}, \dots, X_{(n-r+1)})
$$
の同時分布や、  
十分大きな閾値 $u$ に対して、 $X | X\gt u$ もしくは、 $X-u | X\gt u$ の分布にも興味がある。

### 極値分布

$Z_n$ の分布を考える。

$$
\begin{align*}
P(Z_n \le x) &= P(\max{\{X_1, X_2 \dots, X_n\}} \le x)\\
&= \prod_{i=1}^n P(X_i \le x)\\
&= \left\{P(X_i\le x)\right\}^n\\
&= \left\{F(x)\right\}^n\\
&= F^n(x)
\end{align*} 
$$

分布関数の性質より $0\le F(x) \le 1$ であるので、$n\to \infty$ のとき
$$
P(Z_n \le x) = F^n(x) \to 
\begin{cases}
0 & (x:\ F(x)\lt 1)\\
1 & (x:\ F(x)=1)
\end{cases}
$$
したがって、 $n\to\infty$ では、$Z_n$ は分布 $F$ の上限 $w_F$ へ収束する。  



そこで、$Z_n$ を退化していない分布へ収束するように、次のような基準化を考える。  
定数列 $a_n\gt 0,\ b_n \in \mathbb{R}\ (n=1, 2, \dots, n)$ 、退化していない分布 $G$ を持つ確率変数 $Z$ が存在して、 $n\to \infty$ のとき
$$
\frac{Z_n-b_n}{a_n}\xrightarrow{d} Z \\[6pt]
\Leftrightarrow\\[6pt]
 P\left(\frac{Z_n-b_n}{a_n}\le x\right) \rightarrow P(Z\le x) = G(x)
$$

となる場合を考える。  

$$
P\left(\frac{Z_n-b_n}{a_n}\le x\right) = P(Z_n \le a_nx+b_n) = F^n(a_nx+b_n)
$$

より
$$
\begin{align}
F^n(a_nx+b_n)\rightarrow  G(x)
\tag{2.4}
\end{align}
$$
である。  
このとき、$G$ 極値分布といい、分布 $F$ は極値分布 $G$ の吸引領域(domain of attraction) に属するといい、$F\in G(x)$ と書く。  

