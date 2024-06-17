# Discrete Fourier Transform (DFT)

DFT:

$$X[k] = \sum_{n=0}^{N-1}x[n]W_N^{kn}\qquad 0 \le k \le N-1$$
IDFT:

$$x[n] = \frac{1}{N}\sum_{k=0}^{N-1}X[k]W_N^{-kn}\qquad 0 \le n \le N-1$$

$$W_N = e^{-j2\pi / N}$$

### Periodicity of DFT

$$X[k+N] = X[k]$$

where $N$ is the length of $x[n]$.

### Relationship between DTFT and DFT

DTFT sampling in frequency domain $\longrightarrow$ DFT: 

$$X[k] = X(e^{j\omega})|_{\omega=2\pi k/N}$$

### Relationship of $\Omega$ (CTFT), $\omega$ (DTFT) and $k$ (DFT)

$$\omega = \Omega T = 2 \pi f T$$
$$\omega_k = (\frac{2\pi}{N})k = 2\pi f_k T$$
$$f_k = \frac{k}{NT}$$

$\frac{1}{NT}$ is called **frequency resolution**.

### DFT symmetry relations

Circular conjugate-symmetry: 

$$x[n] = x^*[\langle-n\rangle_N] = x^*[\langle N-n\rangle_N] \quad 0 \le n \le N-1$$

Circular conjugate-antisymmetry:

$$x[n] = -x^*[\langle-n\rangle_N] = -x^*[\langle N-n\rangle_N] \quad 0 \le n \le N-1$$

A length-N sequence can be expressed as a sum of its circular conjugate-symmetric part and its circular conjugate-antisymmetric part.

$$x[n] = x_{pcs}[n] + x_{pca}[n]$$

$$x_{pcs}[n] = (x[n] + x^*[\langle -n \rangle_N]) / 2$$

$$x_{pca}[n] = (x[n] - x^*[\langle -n \rangle_N]) / 2$$
Geometric symmetry: 

$$x[n] = x[N-1-n] \quad 0 \le n \le N-1$$

Geometric antisymmetry:

$$x[n] = -x[N-1-n] \quad 0 \le n \le N-1$$

| sequence                    | DFT                                                        |
| --------------------------- | ---------------------------------------------------------- |
| $x^*[n]$                    | $X^*[\langle -k \rangle_N]$                                |
| $x^*[\langle -n \rangle_N]$ | $X^*[k]$                                                   |
| $Re\{x[n]\}$                | $X_{pcs}[k] = \frac{1}{2}\{X[k]+X^*[\langle-k\rangle_N]\}$ |
| $jIm\{x[n]\}$               | $X_{pca}[k] = \frac{1}{2}\{X[k]-X^*[\langle-k\rangle_N]\}$ |
| $x_{pcs}[n]$                | $Re\{X[k]\}$                                               |
| $x_{pca}[n]$                | $jIm\{X[k]\}$                                              |

### Circular convolution

$$y_C[n] = g[n]\textcircled{N}h[n] = \sum_{m=0}^{N-1}g[m]h[\langle n-m\rangle_N]$$

