# Control Volume

A thermodynamic system where energy and matter is exchanged across its boundary.

## Key variables

### Mass Flow Rate
Mass flow rate, $\dot{m} = \frac{dm}{dt} = \rho\dot{V} = \rho AV$  
Unit for mass flow rate: kg s<sup>-1</sup>  

### Density
Density, $\rho = \frac{mass}{volume}$ <br>
Unit for density: kg m<sup>-3</sup>  

### Specific Volume
Specific volume, $\nu = \frac{1}{\rho}$ <br>
Unit for specific volume: m<sup>3</sup> kg<sup>-1</sup>  

### Volumetric flow rate
Volumetric flow rate, $\dot{V} = AV$ <br>
Unit for volumetric flow rate: m<sup>3</sup> s<sup>-1</sup>

## Conservation of Mass

At steady state, $\frac{dm_{cv}}{dt} = 0$. <br>
$\therefore \sum\limits_{i}\dot{m}_{i} = \sum\limits_{e}\dot{m}_{e}$

where: 

* $m_{cv}$ is the mass of the control volume; and
* $\dot{m}_{i}$ and and $\dot{m}_{e}$ are the mass flow rates at the inlets and exits.
	
## Work for a Control Volume

For a control volume with multiple inlets and exits, the work term $\dot{W}$ of a control volume is:

$$
\dot{W} = \dot{W}_{cv}+\sum\limits_{e}\dot{m}_{e}\left(p_{e}\nu_{e}\right)-\sum\limits_{i}\dot{m}_{i}\left(p_{i}\nu_{i}\right)
$$

where: 

* $\dot{m}_{i}$ and and $\dot{m}_{e}$ are the mass flow rates at the inlets and exits;  
* $\nu_{i}$ and $\nu_{e}$ are the specific volumes at the inlets and exits;  
* $\dot{m}_{i}\left(p_{i}\nu_{i}\right)$ and $\dot{m}_{e}\left(p_{e}\nu_{e}\right)$ are the flow work at the inlets and exits; and  
* $\dot{W}_{cv}$ is the shaft work across the boundary of the control volume.<br>

### Flow and Shaft Work
* Flow work is due to the fluid pressure as the mass enters and exits the control volume.  
* Shaft work occurs due to rotating shafts, displacement of boundary or electrical effects.

## Conservation of Energy for a Control Volume

For a control volume with multiple inlets and multiple exits, the energy rate balance is:

$$  
\begin{align*}
\frac{dE_{cv}}{dt} &= \dot{Q}_{cv}-\dot{W}_{cv}+\sum\limits_{i}\dot{m}_{i}\left(u_{i}+p_{i}\nu_{i}+\frac{V_{i}^2}{2}+gz_{i}\right)-\sum\limits_{e}\dot{m}_{e}\left(u_{e}+p_{i}\nu_{i}+\frac{V_{e}^2}{2}+gz_{e}\right) \\  
&= \dot{Q}_{cv}-\dot{W}_{cv}+\sum\limits_{i}\dot{m}_{i}\left(h_{i}+\frac{V_{i}^2}{2}+gz_{i}\right)-\sum\limits_{e}\dot{m}_{e}\left(h_{e}+\frac{V_{e}^2}{2}+gz_{e}\right) \\
&\because \text{Specific enthalpy, }h = u + p\nu
\end{align*}
$$

where: 

* $\dot{E}_{cv}$ denotes the energy of control volume at time t;  
* $\dot{Q}$ denotes the net rate of heat transfer at time t;  
* $\dot{W}$ denotes the work across the boundary of the control volume at time t;  
* $\dot{m}_{i}u_{i}$ and $\dot{m}_{e}u_{e}$ denotes the rate of transfer of internal energy of the multiple inlets and exits;  
* $\dot{m}_{i}\frac{V_{i}^{2}}{2}$ and $\dot{m}_{e}\frac{V_{e}^{2}}{2}$ denotes the rate of transfer of kinetic energy of the multiple inlets and exits; and 
* $\dot{m}_{i}gz_{i}$ and $\dot{m}_{e}gz_{e}$ denotes the rate of transfer of graviational potential energy of the multiple inlets and exits. <br>
<br>
Assuming specifc heat capacity at constant pressure $c_{p}$ is **independent of temperature**:  

$$
h_{2} - h_{1} = c_{p}\left(T_{2}-T_{1}\right)
$$

## Applications of Control Volumes

### Nozzles and Diffusers

- Nozzles _increase_ the velocity of fluid in the direction of fluid flow.
- Diffusers _decrease_ the velocity of fluid in the direction of fluid flow.

$$ 
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\limits_{i}\dot{m}_{i}\left(h_{i}+\frac{V_{i}^2}{2}+gz_{i}\right)-\sum\limits_{e}\dot{m}_{e}\left(h_{e}+\frac{V_{e}^2}{2}+gz_{e}\right) \\  
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\dot{m}\left[\left(h_{i}-h_{e}\right)+\frac{V_{i}^2-V_{e}^2}{2}+\left(gz_{i}-gz_{e}\right)\right] \\  
\because \sum\limits_{i}\dot{m}_{i} = \sum\limits_{e}\dot{m}_{e} \ \text{at steady state}\\
\Rightarrow 0 = (h_{1}-h_{2})+\frac{V_{1}^{2}-V_{2}^{2}}{2}
$$

* Net rate of energy $\frac{dE_{cv}}{dt} = 0$ at steady state;  
* Net rate of heat transfer $\dot{Q}_{cv}$ is negligible;
* There is no shaft work $\dot{W}_{cv}$;  
* There is only flow work; and
* Change in potential energy $\sum\dot{m}\left(gz_{i}-gz_{e}\right)$ is negligble.

### Turbines

- Turbines generate power when fluids pass through blades attached to a shaft, which can freely rotate.

$$ 
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\limits_{i}\dot{m}_{i}\left(h_{i}+\frac{V_{i}^2}{2}+gz_{i}\right)-\sum\limits_{e}\dot{m}_{e}\left(h_{e}+\frac{V_{e}^2}{2}+gz_{e}\right) \\  
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\dot{m}\left[\left(h_{i}-h_{e}\right)+\frac{V_{i}^2-V_{e}^2}{2}+\left(gz_{i}-gz_{e}\right)\right] \\  
\Rightarrow \dot{W}_{cv} = \dot{m}\left(h_{1}-h{2}\right)
$$

* Net rate of energy $\frac{dE_{cv}}{dt} = 0$ at steady state; 
* Stray heat transfer $\dot{Q}_{cv}$ is negligible;
* Change in kinetic energy $\sum\dot{m}\left(\frac{V_{i}^2-V_{e}^2}{2}\right)$ is negligible; and
* Change in potential energy $\sum\dot{m}\left(gz_{i}-gz_{e}\right)$ is negligble.

### Compressors and Pumps

- Compressors do work on _gases_ to change the state of gases.
- Pumps do work on _liquids_ to change the state of liquids.

$$ 
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\limits_{i}\dot{m}_{i}\left(h_{i}+\frac{V_{i}^2}{2}+gz_{i}\right)-\sum\limits_{e}\dot{m}_{e}\left(h_{e}+\frac{V_{e}^2}{2}+gz_{e}\right) \\  
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\dot{m}\left[\left(h_{i}-h_{e}\right)+\frac{V_{i}^2-V_{e}^2}{2}+\left(gz_{i}-gz_{e}\right)\right] \\  
\Rightarrow \dot{W}_{cv} = \dot{m}\left(h_{1}-h_{2}\right) \\
\because \dot{W}_{cv} < 0, \ \therefore \text{power input required}
$$

* Net rate of energy $\frac{dE_{cv}}{dt} = 0$ at steady state;
* Stray heat transfer $\dot{Q}_{cv}$ is negligible;
* Change in kinetic energy $\sum\dot{m}\left(\frac{V_{i}^2-V_{e}^2}{2}\right)$ is negligible; and
* Change in potential energy $\sum\dot{m}\left(gz_{i}-gz_{e}\right)$ is negligble.

### Heat Exchangers

- Heat exchangers transfer heat between two or more fluids.

$$ 
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\limits_{i}\dot{m}_{i}\left(h_{i}+\frac{V_{i}^2}{2}+gz_{i}\right)-\sum\limits_{e}\dot{m}_{e}\left(h_{e}+\frac{V_{e}^2}{2}+gz_{e}\right) \\  
\frac{dE_{cv}}{dt} = \dot{Q}_{cv}-\dot{W}_{cv}+\sum\dot{m}\left[\left(h_{i}-h_{e}\right)+\frac{V_{i}^2-V_{e}^2}{2}+\left(gz_{i}-gz_{e}\right)\right] \\ 
\Rightarrow 0 = \dot{Q}_{cv} + \sum\limits_{i}\dot{m}_{i}h_{i}-\sum\limits_{e}\dot{m}_{e}h_{e}
$$

* Net rate of energy $\frac{dE_{cv}}{dt} = 0$ at steady state;
* There is no shaft work $\dot{W}_{cv}$;  
* There is only flow work;
* Change in kinetic energy $\sum\dot{m}\left(\frac{V_{i}^2-V_{e}^2}{2}\right)$ is negligible; and
* Change in potential energy $\sum\dot{m}\left(gz_{i}-gz_{e}\right)$ is negligible.

## Change in Specific Entropy for Ideal Gases

$$
\Delta s_{1\rightarrow 2} = s_{2}-s_{1}=c_{v}\ln\left(\frac{T_{2}}{T_{1}}\right)-r \ln\left(\frac{V_{2}}{V_{1}}\right)\\
\Delta s_{1\rightarrow 2} = s_{2}-s_{1}=c_{p}\ln\left(\frac{T_{2}}{T_{1}}\right)-r \ln\left(\frac{P_{2}}{P_{1}}\right)\\
\Delta s_{1\rightarrow 2} = s_{2}-s_{1}=c_{p}\ln\left(\frac{V_{2}}{V_{1}}\right)-c_{v} \ln\left(\frac{P_{2}}{P_{1}}\right)\\
$$