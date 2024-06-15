# Operations on sequences

## Elementary Operations

### product

$$w_1[n] = x[n]\cdot y[n]$$

also called **Modulation(调制)**

![](../attachments/Pasted%20image%2020240615111432.png)

### scalar multiplication

$$w_2[n] = Ax[n]$$

![](../attachments/Pasted%20image%2020240615111538.png)

### addition

$$w_3[n] = x[n]+y[n]$$

![](../attachments/Pasted%20image%2020240615111627.png)

### Time-shifting

$$w_4[n] = x[n-N]$$

Unit delay(单位延迟): 

$$w[n] = x[n-1]$$

![](../attachments/Pasted%20image%2020240615111825.png)

Unit advance(单位超前):

$$w[n] = x[n+1]$$

![](../attachments/Pasted%20image%2020240615111856.png)

### Time-reversal

$$w_5[n]= x[-n]$$

Also called **folding operation**

## Convolution sum

$$y[n] = x[n] * h[n] = \sum_{k=-\infty}^{\infty}x[k]h[n-k]$$

## Sampling rate alteration(抽样率转换)

Let sampling frequency for $x[n]$ be $f_1$ and for $y[n]$ be $f_2$ .

$$R = \frac{f_2}{f_1}$$

if $R>1$, **interpolation(内插)**; if $R<1$, **decimation(抽取)** 

up-sampling: 

![](../attachments/Pasted%20image%2020240615113722.png)

$$y[n] = \begin{cases}
x[n/L], &n=0,\pm L, \pm2L, ...\\
0, &others
\end{cases} $$

down-sampling: 

![](../attachments/Pasted%20image%2020240615113727.png)

$$y[n] = x[nM]$$

## Circular operation(圆周运算)

### Circular time-reversal operation(圆周反转运算)

For a finite-length sequence $x[n]$ defined on $0 \le n \le N-1$ with length $N$，if $\langle m \rangle_N = m \mod N$, then the circular time-reversal operation is defined as $y[n]=x[\langle -n\rangle_N] \quad for \quad 0 \le n \le N-1$.

e.g. $x[n] = n+1, \quad 0 \le n \le 5 \quad N=6$

$$\begin{align}
y[0] = x[\langle0\rangle_6]=x[0] \\
y[1] = x[\langle-1\rangle_6]=x[5] \\
y[2] = x[\langle-2\rangle_6]=x[4] \\
y[3] = x[\langle-3\rangle_6]=x[3] \\
y[4] = x[\langle-4\rangle_6]=x[2] \\
y[5] = x[\langle-5\rangle_6]=x[1] \\
\end{align}$$
### Circular shift of a sequence(序列的圆周平移)

if $n_0 \ge 0$

$$x_c[n] = x[\langle n-n_0\rangle_N] = \begin{cases}x[n-n_0] \quad &n_0 \le n \le N-1 \\ x[N-n_0+n] \quad &0\le n < n_0\end{cases}$$

e.g.

![](../attachments/Pasted%20image%2020240615115540.png)

## Classification of sequences

### Conjugate-symmetric sequence vs Conjugate-antisymmetric sequence

Conjugate-symmetric sequence: $x[n] = x^*[-n]$

Conjugate-antisymmetric sequence: $x[n] = -x^*[-n]$

Real conjugate-symmetric sequence is called **even sequence**.

Real conjugate-antisymmetric sequence is called **odd sequence**.

> for conjugate-antisymmetric sequence, $x[0]$ must be pure imaginary number(纯虚数), for odd sequence, $x[0]=0$.

Any complex sequence can be expressed as a sum of its conjugate-symmetric part and its conjugate-antisymmetric part.

$$x[n] = x_{cs}[n] + x_{ca}[n]$$

$$x_{cs}[n] = \frac{1}{2}(x[n] + x^*[-n])$$

$$x_{cs}[n] = \frac{1}{2}(x[n] + x^*[-n])$$

### Periodic sequence vs Aperiodic sequence

Periodic sequence： $\widetilde{x}[n] = \widetilde{x}[n+kN]$

### Energy signal vs Power signal

Total energy of a sequence: 

$$\mathscr{E} = \sum_{n=-\infty}^{\infty}|x[n]|^2$$

Average power of an aperiodic sequence: 

$$\mathscr{P}=\lim_{k \rightarrow\infty}\frac{1}{2K+1}\sum_{n=-K}^{K}|x[n]|^2$$

Average power of a periodic sequence with a period $N$:

$$\mathscr{P} = \frac{1}{N}\sum_{n=0}^{N-1}|x[n]|^2$$

### Bounded sequence vs absolutely summable sequence

absolutely summable(绝对可和):

$$\sum_{n=-\infty}^{\infty}|x[n]|<\infty$$

square-summable(平方可和): 

$$\sum_{n=-\infty}^{\infty}|x[n]|^2<\infty$$
