# LTI discrete-time systems

## Representations of LTI discrete-time systems

### Impulse response

Classification:

- FIR (Finite impulse response)
- IIR (Infinite impulse response)

#### FIR

$$h[n]=0, \quad n < N_1 \quad and \quad n > N_2$$
$$y[n] = \sum_{k=N_2}^{N_1}h[k]x[n-k]$$

#### IIR

$$y[n] = \sum_{k=-\infty}^{\infty}x[k]h[n-k]$$

### Linear Constant-Coefficient Difference Equation

Difference equation: 

$$\sum_{l=0}^{N}d_ly[n-l] = \sum_{k=0}^{M}p_kx[n-k]$$

Classification:

- Non-recursive system
- Recursive system

#### Non-recursive system

$$y[n] = \sum_{k=0}^{M}p_kx[n-k]$$

No feedback from the output

#### Recursive system

Self-feedback:

$$y[n] = -\sum_{l=1}^{N}d_ly[n-l]$$

General case, with feedback:

$$y[n] = \sum_{k=0}^{M}p_kx[n-k] - \sum_{l=0}^{N}d_ly[n-l]$$

#### Some commonly used system models

##### Moving average(MA)

$$y[n] = \sum_{k=0}^{M}p_kx[n-k]$$

FIR system, non-recursive system

##### Autoregressive (AR)

$$y[n] = x[n] -\sum_{k=1}^{N}d_ky[n-k]$$

IIR system, recursive system

##### Autoregressive moving average (ARMA)

$$y[n] = \sum_{k=0}^{M}p_kx[n-k] - \sum_{k=1}^{N}d_ky[n-k]$$

### Frequency response

$$y[n] = x[n] * h[n]$$

$$Y(e^{j\Omega}) = H(e^{j\Omega})X(e^{j\Omega})$$

Frequency response:

$$H(e^{j\Omega}) = \frac{Y(e^{j\Omega})}{X(e^{j\Omega})}$$

Amplitude response: 

$$|H(e^{j\Omega})|$$

Phase response:

$$\theta(\omega) = \arg\{H(e^{j\Omega})\}$$

FIR: 

$$H(e^{j\Omega}) = \sum_{n=N_1}^{N_2}h[n]e^{-j\omega n}$$

IIR: 

$$H(e^{j\Omega}) = \frac{Y(e^{j\Omega})}{X(e^{j\Omega})} = \frac{\sum_{k=1}^{M}p_ke^{-j\omega k}}{\sum_{k=1}^{N}d_ke^{-j\omega k}}$$
