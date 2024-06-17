# Definition of z-transform

$$X(z) = Z\{x[n]\} = \sum_{n=-\infty}^{\infty}x[n]z^{-n}$$

## Shape of ROC

right-sided sequences:

ROC: $|z|>R_{x-}$

![](../attachments/Pasted%20image%2020240617152918.png)

left-sided sequences:

ROC: $|z|<R_{x+}$

![](../attachments/Pasted%20image%2020240617152956.png)

two-sided sequences:

ROC: $R_{x-}<|z|<R_{x+}$

![](../attachments/Pasted%20image%2020240617153125.png)

## Commonly used z-transform pairs


| sequence               | z-transform                                 | ROC                |
| ---------------------- | ------------------------------------------- | ------------------ |
| $\delta[n]$            | 1                                           | All values of z    |
| $\mu[n]$               | $\frac{1}{1-z^{-1}}$                        | $\|z\|>1$          |
| $\alpha^n\mu[n]$       | $\frac{1}{1-\alpha z^{-1}}$                 | $\|z\|>\|\alpha\|$ |
| $n\alpha^n \mu[n]$     | $\frac{\alpha z^{-1}}{(1-\alpha z^{-1})^2}$ | $\|z\|>\|\alpha\|$ |
| $(n+1)\alpha^n \mu[n]$ | $\frac{1}{(1-\alpha z^{-1})^2}$             | $\|z\|>\|\alpha\|$ |
