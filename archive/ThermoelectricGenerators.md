# Thermoelectric Generators

## Principles of Thermoelectricity

### Seebeck effect

Seebeck effect is a phenomenon when a temperature difference between two different metal conductors results in an induced voltage, $\Delta V_{se}$, where:

$$  
|\Delta V_{se}| = |S_{e}\Delta T|
$$  

<center>Typical units of Seebeck coefficient, $S_{e}: \mu \text{V/K}$ </center>

* Seebeck coefficient: describes thermoelectric capability of material  
	* $S_{e} > 0$: p-type semiconductor (current, heat carried by positively charged holes)  
	* $S_{e} > 0$: Platinum (reference metal) 
	* $S_{e} > 0$: n-type semiconductor (current, heat carried by negatively charged electrons)

### Peltier effect

Peltier effect is a phenomenon when temperature difference is induced due to current flow.

$$  
\dot{Q} = S_{e}IT, \text{where} \ \pi = S_{e}T
$$  

<center>and T is the temperature of the interface where the current flows</center>

### Ohm's Law and Joule Heating

* Ohm's Law $V = IR \ \text{where} \ R= \frac{\rho l}{A}$  
* Joule heating is isotropic  
	* 50% to top, 50% to bottom

### Thermal Conduction

* Due to thermal conductivity of material

$$  
\begin{align*}
\dot{Q} &= \kappa A \frac{T_{h}-T_{c}}{l}  \\
&= \frac{\kappa A}{l}\Delta T \\
&= \lambda \Delta T
\end{align*}
$$

## Thermoelectric Generator vs Thermomechanical Heat Engine

* TEG: Converts thermal energy to electrical energy to do work  
	* Difference in temperature creates a potential difference (Seebeck effect)<br>
<br>
* Heat engine: Converts thermal energy to do work  
	* Operates between thermal reservoirs of different temperatures ($T_{hot}$, $T_{cold}$)
	* Takes $Q_{h}$ from hot reservoir, converts some to work, the rest goes to cold reservoir via $Q_{c}$

## Thermoelectric Figure of Merit

$$
\begin{align*}
Z &= \frac{S^{2}_{e}}{R_{in}\lambda} = \frac{\text{material property}^{2}}{\text{(electrical resistance)(thermal conductance)}} \\
T &= \frac{T_{h}+T_{c}}{2}  \\
\Rightarrow ZT &= \frac{S^{2}_{e}}{R_{in}\lambda}\left(\frac{T_{h}+T_{c}}{2}\right) = \frac{S^{2}_{e}\sigma}{\kappa}\left(\frac{T_{h}+T_{c}}{2}\right)
\end{align*}
$$

where:  

* $R_{in}$ is internal resistance of the TEG; $R_{in}=\frac{\rho l}{A}$
* $\lambda$ is the thermal conductance of the TEG; $\lambda = \frac{\kappa A}{l}$
* $\sigma$ is the electrical conductivity of the TEG; $\sigma = \frac{1}{\rho}$
* $\kappa$ is the thermal conductivity of the TEG. 

## Electrical Analysis of TEG

$$  
\begin{align*}
\text{Voltage drop across } R_{L}, V &= \Delta V_{Se} - IR_{in} \\
&= |S_{e}\left(T_{h} - T_{c}\right)| - IR_{in}\\
\text{Power delivered by TEG, }\dot{W} &= IV \\
&= |S_{e}I\left(T_{h} - T_{c}\right)| - I^{2}R_{in}
\end{align*}
$$

!!! tip
	The power delivered by the TEG has to match the power received by $R_{L}$, where $\dot{W} = I^{2}R_{L}$.
	
## Energy Flow of TEG

$$  
\begin{align*}
\dot{Q}_{h} &= S_{e}IT_{h}-\frac{I^{2}R_{in}}{2}+\lambda\left(T_{h}-T_{c}\right)  \\
\dot{Q}_{c} &= S_{e}IT_{c}+\frac{I^{2}R_{in}}{2}+\lambda\left(T_{h}-T_{c}\right)  \\
\text{By First Law: }\dot{W} &= \dot{Q}_{h}-\dot{Q}_{c} \\
&= S_{e}I\left(T_{h}-T_{c}\right)-I^{2}R_{in} 
\end{align*}
$$

## Efficiency of TEG

$$  
\begin{align*}
\text{Efficiency, }\eta &= \frac{\text{desired output}}{\text{required input}} \\
&= \frac{W_{cycle}}{Q_{h}}= \frac{Q_{h}-Q_{c}}{Q_{h}}\\
&= 1-\frac{Q_{c}}{Q_{h}}\\
\end{align*}
$$

Applying Second Law: 

$$
\frac{dS}{dt} = \frac{\dot{Q}_{in}}{T_{in}}-\frac{\dot{Q}_{out}}{T_{out}}+\dot{\sigma}_{gen} = 0
$$

**Assuming reversible process,** 

$$
\dot{\sigma}_{gen} = 0 \\
\Rightarrow 0 = \frac{\dot{Q}_{h}}{T_{h}}+\frac{\left(-\dot{Q}_{c}\right)}{T_{c}}
$$

Applying First Law: 

$$
\dot{W} = \dot{Q}_{h}-\dot{Q}_{c}\\
0 = \frac{\dot{Q}_{h}}{T_{h}} + \frac{-\left(\dot{Q}_{h}-\dot{W}\right)}{T_{c}}\\
\Rightarrow \dot{W} = \dot{Q}_{h}\left(1-\frac{T_{c}}{T_{h}}\right)\\
\text{Carnot efficiency, }\eta_{carnot} = \frac{\dot{W}}{\dot{Q}_{h}} = 1-\frac{T_c}{T_{h}} \\ \text{(Theoretical maximum efficiency of engine with $T_{c}$ and $T_{h}$})
$$

### Calculating Efficiency of TEG by Thermoelectric Properties and ZT

$$  
\begin{align*}
\text{Efficiency, }\eta &= \frac{W_{cycle}}{Q_{h}}\\
&= \frac{S_{e}I\left(T_{h}-T_{c}\right)-I^{2}R_{in}}{S_{e}IT_{h}-\frac{I^{2}R_{in}}{2}+\lambda\left(T_{h}-T_{c}\right)}
\end{align*} 
$$

<center>If $\lambda \rightarrow 0, R_{in} \rightarrow 0, \eta \rightarrow \frac{T_{h}-T_{c}}{T_{h}} = 1-\frac{T_{c}}{T_{h}}$  <b>(Carnot efficiency)</b></center><br>
Using ZT: 

$$
\eta_{carnot} = \left(\frac{T_{h}-T_{c}}{T_{h}}\right)\left(\frac{\sqrt{1+ZT}-1}{\sqrt{1+ZT}+\frac{T_{c}}{T_{h}}}\right)
$$

## Load Resistance for Maximum Power Output

$$
V_{out} = IR_{L} = \frac{\Delta V_{se}}{(R_{in}+R_{L})}R_{L}\\
\dot{W} = \frac{V_{out}^{2}}{R_{L}} = \frac{\Delta V_{se}^{2}R_{L}}{(R_{in}+R_{L})^{2}}\\
\text{To find minimum or maximum, }\frac{d\dot{W}}{dR_{L}} = 0.\\
\Rightarrow \frac{\Delta V_{se}^{2}}{(R_{in}+R_{L})^{2}} + \frac{\Delta V_{se}^{2}R_{L}(-2)}{(R_{in}+R_{L})^{3}} = 0\\
R_{in} + R_{L} - 2R_{L} = 0 \ \mathbf{\Rightarrow R_{in} = R_{L}}.\\
\text{To check if minimum or maximum occurs when }R_{in} = R_{L}\text{, find }\frac{d\dot{W}}{dR_{L}}.\\
\frac{d\dot{W}}{dR_{L}} = -\frac{4\Delta V_{se}^{2}}{(R_{in}+R_{L})^{3}}+\frac{6\Delta V_{se}^{2}R_{L}}{(R_{in}+R_{L})^{4}}\\
\text{When }R_{L} = R_{in}: \frac{d\dot{W}}{dR_{L}} = -\frac{2\Delta V_{se}^{2}}{16R_{in}} < 0\\
\therefore \dot{W}_{max}\text{ when }R_{L} = R_{in}
$$

## Analysing electrical power

* More $\dot{W}$ can be obtained with larger $\Delta T$
* $I_{@\dot{W}_{max}} > I_{@\eta_{max}}$ slightly
	* Which current to use depends on what is required

## Effective Parameters of Thermoelectric Device

* TE device consists of multiple TE elements:

$$
\text{Effective }S_{e} = N(S_{e,p} - S_{e,n})\\
\text{Effective }R_{in} = N(R_{p}+R_{n})\\
\text{Effective }\lambda = N(\lambda_{p}+\lambda_{n})
$$

## Thermal Contacts

* Actual temperature at surface of semiconducting elements is not what is applied at the ends
* $\Delta T$ exists due to thermal conductance of ceramic plates and metal leads

## Practical Thermoelectric Devices

* Match $\dot{Q}_{c}$ with required cooling power
* Match $\dot{Q}_{h}$ with heat sink