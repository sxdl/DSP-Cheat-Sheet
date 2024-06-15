# Continuous-time Fourier transform

## CTFT

$$x(t)\stackrel{CTFT}{\longleftrightarrow}X(j\Omega)$$
Direct transform:

$$X(j\Omega) = \int_{-\infty}^{+\infty}x(t)e^{-j\Omega t}dt$$

Inverse transform:

$$x(t) = \frac{1}{2\pi}\int_{-\infty}^{+\infty}X(j\Omega)e^{j\Omega t}d\Omega$$

Base on 

$$X(j\Omega) = |X(j\Omega)|e^{j\theta(\Omega)}$$

$$\theta(\Omega) = \arg\{X(j\Omega)\}$$

magnitude spectrum(幅度谱): $|X(j\Omega)|$

phase spectrum(相位谱): $\theta(\Omega)$

## Energy Density Spectrum

Total energy of a signal: 

$$\mathscr{E} = \int_{-\infty}^{\infty}|x(t)|^2dt$$

Parseval’s theorem: 

$$\int_{-\infty}^{\infty}|x(t)|^2dt = \frac{1}{2\pi}\int_{-\infty}^{\infty}|X(j\Omega)|^2d\Omega$$

Energy Density Spectrum: 

$$S_{xx}(\Omega) = |X(j\Omega)|^2$$

## Band-limited continuous-time signals

|              | Frequency range                                         | bandwidth(带宽)          |
| ------------ | ------------------------------------------------------- | ---------------------- |
| Lowpass(低通)  | $0 \le \|\Omega\| \le \Omega_P < \infty$                | $\Omega_P$             |
| Highpass(高通) | $0 \lt \Omega_P \le \|\Omega\| < \infty$                | $\Omega_P$ to $\infty$ |
| Bandpass(带通) | $0 \lt \Omega_L \le \|\Omega\| \le \Omega_H \lt \infty$ | $\Omega_H - \Omega_L$  |
