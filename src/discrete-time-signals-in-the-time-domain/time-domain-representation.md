# Time-domain representation

Continuous-time signal: $x(t)$

Discrete-time signal: $x[n]$

obtained $x[n]$ by sampling $x(t)$ with period $T$ or frequency $f = \frac{1}{T}$

$$ x[n] = x(t) |_{t=nT} = x(nT) $$

![](../attachments/Pasted%20image%2020240615104319.png)

## Length of a discrete-time signal

### Finite-length

$$N=N_2-N_1+1$$

![](../attachments/Pasted%20image%2020240615104625.png)

### Infinite-length

#### Left-sided sequence(左边序列)

also **Anticausal sequence(反因果序列)**

![](../attachments/Pasted%20image%2020240615104634.png)

#### Right-sided sequence(右边序列)

also **Causal sequence(因果序列)**

![](../attachments/Pasted%20image%2020240615104643.png)

#### Two-sided sequence(双边序列)

![](../attachments/Pasted%20image%2020240615104651.png)

## Strength of a discrete-time signal

use $\mathscr{L}_p$-norm: 

$$\Vert x \Vert_p = (\sum_{n=-\infty}^{\infty}|x[n]|^p)^{1/p}$$

typically,

$$\Vert x\Vert_\infty=\max_n|x[n]|$$

$$\frac{\Vert x\Vert_1}{\sqrt{N}} = mean(|x[n]|)$$

$$\frac{\Vert x\Vert_2}{\sqrt{N}} = rms(|x[n]|)$$

> rms(均方根)
