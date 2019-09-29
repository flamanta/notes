# Geometrical Optics

* Approximate method to determine wave propogation
* Also known as *ray optics*

## Fermat's Principle
The optical distance between any 2 points $P_{1}$ and $P_{2}$ is an extremum (usually a minumum).

$$
\begin{align}
\text{Path length, }S &= cT\\
\text{where }S &= \int_{A}^{B}n \ ds\\
\therefore \delta S &= \delta\int_{P_{1}}^{P_{2}}n(s) \ ds = 0
\end{align}
$$

!!! note
	$n(s)$ is the index of refraction of medium.
	
	If the medium is homogeneous, then $n(s) = n = \text{constant}$, and the path will be a straight line.

## Eikonal Surfaces 

- In the form $\psi_{n}(x, y, z), n = 0, 1, 2, 3,...$

- Eikonal equation:

$$
||\nabla\psi_{n}(x, y, z)||^{2}=\left[\frac{\partial\psi_{n}}{\partial x}\right]^{2}+\left[\frac{\partial\psi_{n}}{\partial y}\right]^{2}+\left[\frac{\partial\psi_{n}}{\partial z}\right]^{2}=n^{2}(s)
$$

!!! tip
	Eikonal surfaces for waves are perpendicular to its radial vectors.

## Conservation of Energy Flux
Radiation density $S_{0}$ at $s = 0$ is related to the radiation density $S$ at $s$ by

$$
S_{0} \ dA_{0} = S \ dA \\ 
\Rightarrow \frac{S(s)}{S_{0}(0)}=\frac{dA_{0}}{dA}
$$

## Far Field of Electric Field
The relationship between the far field of an electric field $\mathbf{E}(r,\theta,\phi)$ and the radiation density $S(r,\theta, \phi)$ is

$$
S(r,\theta,\phi) = \frac{1}{2\eta}|\mathbf{E}(r,\theta,\phi)|^{2} = \frac{1}{2}\sqrt{\frac{\epsilon}{\mu}}|\mathbf{E}(r,\theta,\phi)|^{2}\\
\therefore \frac{|\mathbf{E}|^{2}}{|\mathbf{E}_{0}|^{2}}= \frac{dA_{0}}{dA}\\
\Rightarrow \left|\frac{\mathbf{E}}{\mathbf{E}_{0}}\right| = \sqrt{\frac{dA_{0}}{dA}}
$$

## Astigmatic Tube of Rays
For a wave which its eikonal surface forms an astigmatic tube of rays, the relationship between electric field intensity will be

$$
\left|\frac{\mathbf{E}}{\mathbf{E}_{0}}\right| = \sqrt{\frac{dA_{0}}{dA}} = \sqrt{\frac{\rho_{1}\rho_{2}}{(\rho_{1}+s)(\rho_{2}+s)}}
$$

If the wave front is spherical, the equation reduces to 

$$
\left|\frac{\mathbf{E}}{\mathbf{E}_{0}}\right| = \frac{\rho_{0}}{\rho_{0}+s}
$$

If the wave front is cylindrical, the equation reduces to

$$
\left|\frac{\mathbf{E}}{\mathbf{E}_{0}}\right| = \sqrt{\frac{\rho_{0}}{\rho_{0}+s}}
$$

If the wave front is planar, the equation reduces to 

$$
\left|\frac{\mathbf{E}}{\mathbf{E}_{0}}\right| = 1
$$

## Phase and Polarization
Phase and polarization information can be introduced using the *Luneberg-Kline high-frequency expansion*.

The electric field for large $\omega$ can be written as the Luneberg-Kline series

$$
\mathbf{E}(\mathbf{R},\omega) = e^{-j\beta_{0}\psi(\mathbf{R})}\sum_{m=0}^{\infty}\frac{\mathbf{E}_{m}(\mathbf{R})}{(j\omega)^{m}}
$$

where $\mathbf{R}$ = position vector<br>
$\quad\quad \beta_{0}$ = phase constant for free space.
<br><br>
The electric field at $s$ can be approximated to be

$$
\mathbf{E}(s)\approx e^{-j\beta_{0}\psi(s)}\mathbf{E}_{0}(s=0)\\
\because \left|\frac{\mathbf{E}(s=0)}{\mathbf{E}_{0}(0)}\right| =  \sqrt{\frac{\rho_{1}\rho_{2}}{(\rho_{1}+s)(\rho_{2}+s)}}, \\
\therefore \mathbf{E}(s) \approx \mathbf{E}_{0}(0)\sqrt{\frac{\rho_{1}\rho_{2}}{(\rho_{1}+s)(\rho_{2}+s)}}e^{-j\beta_{0}\psi(s)}\\
\Rightarrow \mathbf{E}(s) \approx \mathbf{E}_{0}^{'}(0)e^{-j\beta_{0}\psi(0)}
\sqrt{\frac{\rho_{1}\rho_{2}}{(\rho_{1}+s)(\rho_{2}+s)}}e^{-j\beta s}
$$

where $\mathbf{E}_{0}^{'}(0)e^{-j\phi_{0}(0)}$ is the field at reference point (s = 0), $\sqrt{\frac{\rho_{1}\rho_{2}}{(\rho_{1}+s)(\rho_{2}+s)}}$ is the spatial attentuation (divergence, spreading factors) and $e^{-j\beta s}$ is the phase factor.<br><br>
In addition, $\mathbf{E}_{0}^{'}(0)$ is the field amplitude at reference point (s = 0) and $\phi_{0}(0)$ is the field phase at reference point (s = 0).