# Quantum Mechanics

## Normalized Schrodinger Equations for Hydrogen Atom

For each combination of quantum numbers ($n, l, m$), the solution of the Schrodinger equation is a product of a radial solution $R(r)$ and an angular solution $Y(\theta, \phi)$ of the form $\Psi(r, \theta, \phi) = R(r) \cdot Y(\theta, \phi)$.

The naming of the atomic orbitals depends on the angular momentum quantum number $l$ and the angular node(s) of the orbital.

To obtain the form required for real atomic orbital plots, linear combination of the complex angular wave functions has to be done such that:

$$
Y_{l, \ norm}^{+m} = \frac{1}{\sqrt{2}}\left(Y^{-|m|}_{1}+(-1)^{m}Y^{|m|}_{1}\right) \text{for } m > 0\\
Y_{l, \ norm}^{-m} = \frac{i}{\sqrt{2}}\left(Y^{-|m|}_{1}-(-1)^{m}Y^{|m|}_{1}\right) \text{for } m < 0
$$

## n = 1, l = 0, m = 0

$$
\begin{align*}
R^{1}_{0}(r) &= 2a^{-\frac{3}{2}} \ \text{exp} \left(-\frac{r}{a}\right) \\
\because m = 0, \therefore Y^{0}_{0}(\theta, \phi) &= \sqrt{\frac{1}{4\pi}}\\
\Rightarrow \Psi_{100}(r, \theta, \phi) &= R^{1}_{0}(r)\cdot Y^{0}_{0}(\theta, \phi) \\
&= \frac{1}{\sqrt{\pi}}a^{-\frac{3}{2}} \ \text{exp} \left(-\frac{r}{a}\right)
\end{align*}
$$

<center>$\because l = 0,\text{ and there are no angular nodes,} \therefore \Psi_{100}(r, \theta, \phi) \text{ describes the 1s orbital.}$</center>
## n = 2, l = 0, m = 0

$$
\begin{align*}
R^{2}_{0}(r) &= \frac{1}{\sqrt{2}}a^{-\frac{3}{2}} \left(1-\frac{r}{2a}\right)\ \text{exp} \left(-\frac{r}{2a}\right) \\
\because m = 0, \therefore Y^{0}_{0}(\theta, \phi) &= \sqrt{\frac{1}{4\pi}} \\
\Rightarrow \Psi_{200}(r, \theta, \phi) &= R^{2}_{0}(r)\cdot Y^{0}_{0}(\theta, \phi) \\
&= \frac{1}{\sqrt{8\pi}}a^{-\frac{3}{2}} \left(1-\frac{r}{2a}\right)\ \text{exp} \left(-\frac{r}{a}\right)
\end{align*}
$$

<center>$\because l = 0, \text{and there are no angular nodes,} \therefore \Psi_{200}(r, \theta, \phi) \text{ describes the 2s orbital.}$</center>
## n = 2, l = 1, m = -1

$$
\begin{align*}
R^{2}_{1}(r) &= \frac{1}{\sqrt{24}}a^{-\frac{3}{2}} \left(\frac{r}{a}\right)\ \text{exp} \left(-\frac{r}{2a}\right)\\
Y^{-1}_{1}(\theta, \phi) &= \sqrt{\frac{3}{8\pi}}\sin \theta \ \text{exp} \ (-i\phi)\\
\because m < 0, \therefore \text{Normalized angular solution, }Y^{-1}_{1, \ norm}(\theta, \phi)&=\frac{i}{\sqrt{2}}\left(Y^{-1}_{1}-(-1)^{-1}Y^{+1}_{1}\right)\\
&=\frac{i}{\sqrt{2}}\left(Y^{-1}_{1}+Y^{+1}_{1}\right)\\\\
&= \frac{i}{\sqrt{2}}\left(\sqrt{\frac{3}{8\pi}}\sin \theta\right)\ (\text{exp} \ (-i\phi) -\ \text{exp} \ (i\phi)) \\
&= -\frac{i}{\sqrt{2}}\left(\sqrt{\frac{3}{8\pi}}\sin \theta\sin\phi\right) \times 2i\\
&= \sqrt{2}\left(\sqrt{\frac{3}{8\pi}}\sin \theta\sin\phi\right)\\
&= \frac{1}{2}\sqrt{\frac{3}{\pi}}\sin \theta\sin\phi
\end{align*}
$$

<center>$\text{When } Y^{-1}_{1, \ norm} = 0, \sin \theta\sin\phi = 0$.  
$\Rightarrow y = 0$ <br>
$\therefore \text{There is one angular node where y = 0, which is the xz nodal plane.}$</center>

$$
\begin{align*}
\Rightarrow \Psi_{21-1}(r, \theta, \phi) &= R^{2}_{1}(r)\cdot Y^{-1}_{1, \ norm}(\theta, \phi) \\
&= \frac{1}{4\sqrt{2\pi}}a^{-\frac{3}{2}} \left(\frac{r}{a}\right)\ \text{exp} \left(-\frac{r}{2a}\right)\sin \theta\sin\phi
\end{align*}
$$

<center>$\because l = 1, \text{and there is an angular node at y = 0} \therefore \Psi_{21-1}(r, \theta, \phi) \ \text{describes the } 2p_{y} \ \text{orbital.}$</center>
## n = 2, l = 1, m = 0

$$
\begin{align*}
R^{2}_{1}(r) &= \frac{1}{\sqrt{24}}a^{-\frac{3}{2}} \left(\frac{r}{a}\right)\ \text{exp} \left(-\frac{r}{2a}\right) \\
\because m = 0, \therefore Y^{0}_{1}(\theta, \phi) &= \sqrt{\frac{3}{4\pi}}cos \theta \\
\end{align*}
$$

<center>$\text{When }Y^{0}_{1} = 0, \cos \theta = 0$.  
$\Rightarrow z = 0$ <br>
$\therefore \text{There is one angular node where z = 0, which is the xy nodal plane.}$</center>

$$
\begin{align*}
\Rightarrow \Psi_{210}(r, \theta, \phi) &= R^{2}_{1}(r)\cdot Y^{1}_{0}(\theta, \phi) \\
&= \frac{1}{4}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}} \left(\frac{r}{a}\right)\ \text{exp} \left(-\frac{r}{2a}\right) \cos \theta
\end{align*}
$$

<center>$\because l = 1, \text{and there is an angular node at z = 0} \therefore \Psi_{210}(r, \theta, \phi) \ \text{describes the } 2p_{z} \ \text{orbital.}$</center>
## n = 2, l = 1, m = +1

$$
\begin{align*}
R^{2}_{1}(r) &= \frac{1}{\sqrt{24}}a^{-\frac{3}{2}} \left(\frac{r}{a}\right)\ \text{exp} \left(-\frac{r}{2a}\right)\\
\because m > 0, \therefore \text{Normalized angular solution, }Y^{+1}_{1, \ norm}(\theta, \phi)&=\frac{1}{\sqrt{2}}\left(Y^{-1}_{1}+(-1)^{1}Y^{+1}_{1}\right)\\
&=\frac{1}{\sqrt{2}}\left(Y^{-1}_{1}-Y^{+1}_{1}\right)\\
&= \frac{1}{\sqrt{2}}\left(\sqrt{\frac{3}{8\pi}}\sin \theta\right)\ (\text{exp} \ (-i\phi) +\ \text{exp} \ (i\phi)) \\
&= \frac{1}{\sqrt{2}}\left(\sqrt{\frac{3}{8\pi}}\sin \theta\cos\phi\right) \times 2\\
&= \sqrt{2}\left(\sqrt{\frac{3}{8\pi}}\sin \theta\cos\phi\right)\\
&= \frac{1}{2}\sqrt{\frac{3}{\pi}}\sin \theta\cos\phi
\end{align*}
$$

<center>$\text{When } Y^{+1}_{1, \ norm} = 0, \sin \theta\cos\phi = 0$.  
$\Rightarrow x = 0$ <br>
$\therefore \text{There is one angular node where x = 0, which is the yz nodal plane.}$</center>

$$
\begin{align*}
\Rightarrow \Psi_{21+1}(r, \theta, \phi) &= R^{2}_{1}(r)\cdot Y^{+1}_{1, \ norm}(\theta, \phi) \\
&= \frac{1}{4\sqrt{2\pi}}a^{-\frac{3}{2}} \left(\frac{r}{a}\right)\ \text{exp} \left(-\frac{r}{2a}\right)\sin \theta\cos\phi
\end{align*}
$$

<center>$\because l = 1, \text{and there is an angular node at x = 0} \therefore \Psi_{21+1}(r, \theta, \phi) \ \text{describes the } 2p_{x} \ \text{orbital.}$</center>
## n = 3, l = 0, m = 0

$$
\begin{align*}
R^{3}_{0}(r) &= \frac{2}{81\sqrt{3}}\left[27-18\left(\frac{r}{a}\right)+2\left(\frac{r}{a}\right)^{2}\right] \ \text{exp} \left(-\frac{r}{3a}\right)\\
Y^{0}_{0}(\theta, \phi) &= \sqrt{\frac{1}{4\pi}}\\
\Psi_{300}(r, \theta, \phi) &= \frac{1}{81\sqrt{3\pi}}a^{-\frac{3}{2}}\left[27-18\left(\frac{r}{a}\right)+2\left(\frac{r}{a}\right)^{2}\right] \ \text{exp} \left(-\frac{r}{3a}\right)
\end{align*}
$$

<center>$\therefore \Psi_{300} (r, \theta, \phi) \text{ describes the }3s\text{ orbital.}$</center>
## n = 3, l = 1, m = -1

$$
\begin{align*}
R^{3}_{1}(r) &= \frac{8}{27\sqrt{6}}a^{-\frac{3}{2}}\left(1-\frac{r}{6a}\right)\left(\frac{r}{a}\right) \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{-1}_{1} &= \sqrt{\frac{3}{8\pi}} \sin\theta \ \text{exp}\left(-i\phi\right)\\
\text{Normalized }Y^{-1}_{1} &= \frac{1}{2}\sqrt{\frac{3}{\pi}} \sin\theta \sin\phi\\
\Psi_{31-1} &= \frac{4}{27}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(1-\frac{r}{6a}\right)\left(\frac{r}{a}\right) \ \text{exp}\left(-\frac{r}{3a}\right)\sin\theta\sin\phi
\end{align*}
$$

<center>$\therefore \Psi_{31-1}(r, \theta, \phi)\text{ describes the }3p_{y}\text{ orbital.}$</center>
## n = 3, l = 1, m = 0

$$
\begin{align*}
R^{3}_{1}(r) &= \frac{8}{27\sqrt{6}}a^{-\frac{3}{2}}\left(1-\frac{r}{6a}\right)\left(\frac{r}{a}\right) \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{0}_{1} &= \sqrt{\frac{3}{4\pi}} \cos\theta\\
\Psi_{310} &= \frac{4}{27}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(1-\frac{r}{6a}\right)\left(\frac{r}{a}\right) \ \text{exp}\left(-\frac{r}{3a}\right)\cos\theta
\end{align*}
$$

<center>$\therefore \Psi_{310}(r, \theta, \phi)\text{ describes the }3p_{z}\text{ orbital.}$</center>
## n = 3, l = 1, m = +1

$$
\begin{align*}
R^{3}_{1}(r) &= \frac{8}{27\sqrt{6}}a^{-\frac{3}{2}}\left(1-\frac{r}{6a}\right)\left(\frac{r}{a}\right) \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{+1}_{1} &= \sqrt{\frac{3}{8\pi}} \sin\theta \ \text{exp}\left(i\phi\right)\\
\text{Normalized }Y^{+1}_{1} &= \frac{1}{2}\sqrt{\frac{3}{\pi}} \sin\theta \cos\phi\\
\Psi_{311} &= \frac{4}{27}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(1-\frac{r}{6a}\right)\left(\frac{r}{a}\right) \ \text{exp}\left(-\frac{r}{3a}\right)\sin\theta\cos\phi
\end{align*}
$$

<center>$\therefore \Psi_{311}(r, \theta, \phi)\text{ describes the }3p_{x}\text{ orbital.}$</center>
## n = 3, l = 2, m = -2

$$
\begin{align*}
R^{3}_{2}(r) &= \frac{4}{81\sqrt{30}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{-2}_{2} &= \sqrt{\frac{15}{32\pi}}\sin^{2}\theta \ \text{exp} \ (-2i\phi)\\
\text{Normalized }Y^{-2}_{2} &= \frac{1}{4}\sqrt{\frac{15}{\pi}}\sin^{2}\theta\sin 2\phi\\
\Psi_{32-2} &= \frac{1}{81}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\sin^{2}\theta\sin 2\phi
\end{align*}
$$

<center>$\therefore \Psi_{32-2}(r, \theta, \phi)\text{ describes the }3d_{xy}\text{ orbital.}$</center>
## n = 3, l = 2, m = -1

$$
\begin{align*}
R^{3}_{2}(r) &= \frac{4}{81\sqrt{30}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{-1}_{2} &= \sqrt{\frac{15}{8\pi}}\cos\theta\sin\theta \ \text{exp} \ (-i\phi)\\
\text{Normalized }Y^{-1}_{2} &= \frac{1}{2}\sqrt{\frac{15}{\pi}}\cos\theta\sin\theta\sin\phi\\
\Psi_{32-1} &= \frac{2}{81}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\cos\theta\sin\theta\sin\phi
\end{align*}
$$

<center>$\therefore \Psi_{32-1}(r, \theta, \phi)\text{ describes the }3d_{yz}\text{ orbital.}$</center>
## n = 3, l = 2, m = 0

$$
\begin{align*}
R^{3}_{2}(r) &= \frac{4}{81\sqrt{30}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{0}_{2} &= \sqrt{\frac{5}{16\pi}}\left(3\cos^{2}\theta -1\right)\\
\Psi_{320} &= \frac{1}{81}\sqrt{\frac{1}{6\pi}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\left(3\cos^{2}\theta -1\right)
\end{align*}
$$

<center>$\therefore \Psi_{320}(r, \theta, \phi)\text{ describes the }3d_{z^{2}}\text{ orbital.}$</center>
## n = 3, l = 2, m = +1

$$
\begin{align*}
R^{3}_{2}(r) &= \frac{4}{81\sqrt{30}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{+1}_{2} &= \sqrt{\frac{15}{8\pi}}\cos\theta\sin\theta \ \text{exp} \ (i\phi)\\
\text{Normalized }Y^{+1}_{2} &= \frac{1}{2}\sqrt{\frac{15}{\pi}}\cos\theta\sin\theta\cos\phi\\
\Psi_{321} &= \frac{2}{81}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\cos\theta\sin\theta\cos\phi
\end{align*}
$$

<center>$\therefore \Psi_{321}(r, \theta, \phi)\text{ describes the }3d_{xz}\text{ orbital.}$</center>
## n = 3, l = 2, m = +2

$$
\begin{align*}
R^{3}_{2}(r) &= \frac{4}{81\sqrt{30}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\\
Y^{+2}_{2} &= \sqrt{\frac{15}{32\pi}}\sin^{2}\theta \ \text{exp} \ (2i\phi)\\
\text{Normalized }Y^{-2}_{2} &= \frac{1}{4}\sqrt{\frac{15}{\pi}}\sin^{2}\theta\cos 2\phi\\
\Psi_{32-2} &= \frac{1}{81}\sqrt{\frac{1}{2\pi}}a^{-\frac{3}{2}}\left(\frac{r}{a}\right)^{2} \ \text{exp}\left(-\frac{r}{3a}\right)\sin^{2}\theta\cos 2\phi
\end{align*}
$$

<center>$\therefore \Psi_{322}(r, \theta, \phi)\text{ describes the }3d_{x^{2}-y^{2}}\text{ orbital.}$</center>