# Fourier Transform

## Fourier Series

$$
\begin{align}
    \text{Fourier series, }x(t)&=\int_{-\infty}^{\infty}c_{k}e^{j2\pi kF_{0}t}\\
    \text{where }c_{k} &= \frac{1}{T_{p}}\int_{T_{p}}x(t)e^{-j2\pi kF_{0}t}\ dt \quad (1)
\end{align}
$$

!!! warning
	Equation (1) is only true when $x(t)$ is periodic and satisfies the Direchlet conditions.

## Direchlet conditions

1. x(t) has a finite number of discontinuities in any period
2. x(t) has a finite number of maxima and minima in any period
3. x(t) is absolutely integrable in any period, i.e.
   
$$
\int_{T_{p}}|x(t)| \ dt < \infty\\
$$

!!! note
	All periodic signals of practical interest satisfy these conditions.
	
## Further Simplification of Fourier Series

If x(t) is real, $c_{k}$ and $c_{-k}$ are complex conjugates.
$$
c_{k} = |c_{k}|e^{j\theta_{k}}, c_{-k} = |c_{k}|e^{-j\theta_{k}}
$$

$$
\therefore \text{Fourier series, }x(t) = c_{0}+2\sum_{k=1}^{\infty}|c_{k}|\cos(2\pi kF_{0}t + \theta_{k})
$$

We know that $\cos(2\pi kF_{0}t + \theta_{k})=\cos(2\pi kF_{0}t)\cos\theta_{k} - \sin (2\pi kF_{0}t)\sin\theta_{k}$,

$$
\begin{align}
\therefore \text{Fourier series, }x(t) &= a_{0}+\sum^{\infty}_{k=1}(a_{k}\cos 2\pi kF_{0}t - b_{k}\cos 2\pi kF_{0}t)\\
\text{where }a_{0} &= c_{0}, \ a_{k} = 2|c_{k}|\cos\theta_{k}, \ b_{k}=2|c_{k}|\sin\theta_{k}
\end{align}
$$

!!! info
	This is commonly expressed in many beginner texts on Fourier transform as:
	
	$$
	\begin{align}
	\text{Fourier series, }f(t) = a_{0} + 				&a_{1}\cos(t)+a_{2}\cos(2t)+a_{3}\cos(3t)+...+a_{n}\cos(nt)\\
	+&b_{1}\cos(t)+b_{2}\cos(2t)+b_{3}\cos(3t)+...+b_{n}\cos(nt)\\
	\end{align}
	$$
    
	$$
	\text{where }a_{0} = \frac{1}{2\pi}\int_{0}^{2\pi}f(t) \ dt,\ a_{t} = \frac{1}{\pi}\int_{0}^{2\pi}f(t)\cos(nt) \ dt,\ b_{t} = \frac{1}{\pi}\int_{0}^{2\pi}f(t)\sin(nt) \ dt
	$$

## Equivalent Forms of Fourier Series

### Fourier Series, x(t)

1. $x(t)=\int_{-\infty}^{\infty}c_{k}e^{j2\pi kF_{0}t}$
2. $x(t) = c_{0}+2\sum_{k=1}^{\infty}|c_{k}|\cos(2\pi kF_{0}t + \theta_{k})$
3. $x(t) = a_{0}+\sum^{\infty}_{k=1}(a_{k}\cos 2\pi kF_{0}t - b_{k}\cos 2\pi kF_{0}t)$, <br>
where $a_{0}= c_{0}, \ a_{k} = 2|c_{k}|\cos\theta_{k}, \ b_{k}=2|c_{k}|\sin\theta_{k}$

### Fourier coefficient
- $c_{k} = \frac{1}{T_{p}}\int_{T_{p}}x(t)e^{-j2\pi kF_{0}t}\ dt$
* when $x(t)$ is periodic and satisfies the Direchlet conditions

## Useful Trigonometrical Identities
$$
\begin{align*}
\text{Sine: }\int_{0}^{2\pi} \sin(mt) \ dt &= \ 0 \text{ for any integer }m \\
\text{Cosine: }\int_{0}^{2\pi} \cos(mt) \ dt &= \ 0 \text{ for any non-zero integer }m \\
\\
\text{Product of sine and cosine: }\int_{0}^{2\pi} \sin(mt) \cos(nt)  \ dt &=  \ 0 \text{ for any integers }m, n \\
\\
\text{Product of sines: }\int_{0}^{2\pi} \sin(mt) \sin(nt)  \ dt &=  \ 0 \text{ when }m \neq n, m \neq -n \\
\int_{0}^{2\pi} \sin^{2}(mt) \ dt &= \pi \text{ for any non-zero integer }m \\
\\
\text{Product of cosines: }\int_{0}^{2\pi} \cos(mt) \cos(nt)  \ dt &=  \ 0 \text{ when }m \neq n, m \neq -n \\
\int_{0}^{2\pi} \cos^{2}(mt) \ dt &= \pi \text{ for any non-zero integer }m \\
\end{align*}
$$

## Fourier Transform Theorems and Properties

### Linearity
$a_{1}x_{1}(n)+a_{2}x_{2}(n)\xrightarrow{\mathscr{F}}a_{1}X_{1}(\omega)+a_{2}X_{2}(\omega).$


### Time shifting
$x(n-k)\xrightarrow{\mathscr{F}}e^{-j\omega k}X(\omega)$.

* Shifting signal in time domain by $k$ changes phase by $-\omega k$.

### Time reversal
$x(-n)\xrightarrow{\mathscr{F}}X(-\omega)$

* When signal is folded about origin in time, phase spectrum undergoes phase reversal

### Convolution
$x_{1}(n) \ x_{2}(n) \xrightarrow{\mathscr{F}} X_{1}(\omega)X_{2}(\omega)$

### Wiener-Khintchine theorem
$r_{xx}(l) \xrightarrow{\mathscr{F}} S_{xx}(\omega)$<br>

* Energy spectral density of an energy signal $S$ is the Fourier transform of its autocorrelation sequence $R$

### Frequency shifting
$e^{j\omega_{0}n}x(n) \xrightarrow{\mathscr{F}} X(\omega-\omega_{0})$<br>

* Multiplying $e^{j\omega_{0}n}$ to $x(n)$ is equivalent to translating $X(\omega)$ by $\omega_{0}$

### Modulation
$x(n)\cos \omega_{0}n \xrightarrow{\mathscr{F}} \frac{1}{2}X(\omega+\omega_{0})+\frac{1}{2}X(\omega-\omega_{0})$

### Multiplication (Windowing theorem)
$x_{1}(n) \ x_{2}(n) \xrightarrow{\mathscr{F}} \frac{1}{2\pi}\int_{-\pi}^{\pi}X_{1}(\lambda) \ X_{2}(\omega-\lambda) \ d\lambda$

### Differentiation in the frequency domain
$nx(n) \xrightarrow{\mathscr{F}} j\frac{dX(\omega)}{d\omega}$

### Conjugation
$x^{*}(n)\xrightarrow{\mathscr{F}}X^{*}(-\omega)$

### Parseval's theorem
$\int_{-\infty}^{\infty}x_{1}(n) \ x_{2}^{*}(n) = \frac{1}{2\pi}\int_{-\pi}^{\pi}X_{1}(\omega) \ X_{2}^{*}(\omega) \ d\omega$