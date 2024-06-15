# Correlation of signals

Cross-correlation sequence between two energy signals $x[n]$ and $y[n]$ is defined as:

$$r_{xy}[\mathscr{l}] = \sum_{n=-\infty}^{\infty}x[n]y[n-\mathscr{l}]$$

If $x[n] = y[n]$， cross-correlation(互相关) → autocorrelation(自相关):

$$r_{xx}[\mathscr{l}] = \sum_{n=-\infty}^{\infty}x[n]x[n-\mathscr{l}]$$
correlation: measure similarity of two signals.

Normalized Cross-correlation:

$$\rho _{xy}[\mathscr{l}] = \frac{r_{xy}[\mathscr{l}]}{\sqrt{r_{xx}[o]r_{yy}[0]}}$$


Normalized autocorrelation:

$$\rho_{xx}[\mathscr{l}] = \frac{r_{xx}[\mathscr{l}]}{r_{xx}[0]}$$

property:

$$r_{yx}[\mathscr{l}] = r_{xy}[-\mathscr{l}]$$
