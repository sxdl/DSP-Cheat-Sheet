# Discrete-time Fourier transform

## DTFT

Direct transform:

$$X(e^{j\omega}) = \sum_{n=-\infty}^{\infty}x[n]e^{-j\omega n}$$

Inverse transform:

$$x[n] = \frac{1}{2\pi}\int_{-\pi}^{\pi}X(e^{j\omega})e^{j\omega n}d\omega$$

notation:

$$x[n]\stackrel{\mathscr{F}}{\longleftrightarrow}X(e^{j\omega n})$$
