# Heat Transfer

## Definitions

- System: what we want to study
- Surroundings: external to system
- Boundary: region between system and surroundings where interactions happen
  <br><br>
- Property: macroscopic characteristic of system
- State: condition of system described by properties
- Process: transformation from one state to another
  <br><br>
- Steady state: when a certain property does not change with time
- Extensive property: overall value is sum of its parts (e.g. mass, volume, energy)
- Intensive property: values are independent of size, extent (e.g. pressure, temperature)

## Thermodynamic Systems

1. Isolated system 
	- No exchange of energy
	- No exchange of matter
2. Closed system
	- Exchange of energy 
	- No exchange of matter
3. Open system/Control volume 
	- Exchange of energy 
	- Exchange of matter

## Work Done and Heat Transfer

### Work Done, W

- W > 0: Work done **BY** system
- W < 0: Work done **ON** system

!!! warning
	Work done is **NOT** a property of the system.

### Heat Transfer, Q

- Q > 0: Heat transfer **TO** system
- Q < 0: Heat transfer **FROM** system

!!! warning
	Heat transfer is **NOT** a property of the system.

### Rate of heat transfer

$$
Q = \int_{t_{1}}^{t_{2}}\dot{Q} \ dt\\
\text{Units: }W\text{ or }Js^{-1}
$$

### Heat flux

- Rate of heat transfer per unit area $\dot{q}$

$$
\dot{Q} = \int_{A}\dot{q} \ dA\\
\text{Units: }Wm^{-2}\text{ or }Js^{-1}m^{-2}
$$

### Adiabatic process

- Thermodynamic process involving no heat transfer with the surroundings

## Conduction

* Occurs within the same medium
* Happens in solids, liquids, gases
* Transfer of energy from energetic to less energetic particles<br>

### Fourier's Law

$$
\text{Heat transfer due to conduction, }\dot{Q}_{x} = -\kappa A\frac{dT}{dx}
$$

where:

* $\kappa$ is the thermal conductivity of the material;
* $A$ is the surface area of the material;
* $\frac{dT}{dx}$ is the temperature gradient across the x-direction.

<center>$\textbf{Assuming linear temperature gradient:}$</center>

$$
\text{Heat transfer due to conduction, }\dot{Q}_{x} = -\kappa A\left(\frac{T_{2}-T_{1}}{L}\right)
$$

where:

* $\kappa$ is the thermal conductivity of the material;
* $A$ is the surface area of the material;
* $T_{1}, T_{2}$ are the respective temperatures at two ends of the material;
* $L$ is the length of the material.

## Radiation

* Happens in solids, liquids, gases
* Emission due to changes in electronic configuration of material

### Stefan-Boltzmann Law

$$
\text{Heat transfer due to radiation, }\dot{Q}_{e} = \epsilon\sigma AT_{b}^{4}
$$

where:

* $\epsilon$ is the emissivity (radiation proportionality) of the material; $0\leq\epsilon\leq1$
* $\sigma$ is the Stefan-Boltzmann constant
* $A$ is the surface area of the material;
* $T_{b}$ is the temperature of the emitting surface.

<center>$\textbf{As such, net heat transfer due to radiation:}$</center>

$$
\text{Net heat transfer due to radiation, }\dot{Q}_{e} = \epsilon\sigma A(T_{h}^4-T_{c}^4), \text{where }T_{h} > T_{c}
$$

where:

* $\epsilon$ is the emissivity (radiation property) of the material; $0\leq\epsilon\leq1$
* $\sigma$ is the Stefan-Boltzmann constant
* $A$ is the surface area of the material;
* $T_{h}, T_{c}$ are the temperature of the hot and cold surfaces respectively.<br>

## Convection

* Occurs between solid and liquid; solid and gas

### Newton's law of cooling

$$
\dot{Q}_{c} = hA(T_{h}-T_{c})
$$

where:

* $h$ is the heat transfer coefficient;
* $A$ is the surface area of the material;
* $T_{h}, T_{c}$ are the temperature of the hot and cold surfaces respectively.

### Heat transfer coefficient, h

* Empirical parameter
* Depends on flow pattern, fluid property, geometry<br><br>
* Forced convection
	* Caused by external device (e.g. fan, pump)
	* Larger h (more efficient)
* Free/natural convection
	* Caused by buoyancy effects (difference in air density)
	* Smaller h (less efficient)

## Laws of Thermodynamics

### First Law of Thermodynamics

* Energy is conserved.

$$
\Delta E = E_{2} - E_{1} = Q - W\\
\frac{dE}{dt} = \dot{Q}-\dot{W}\\
dE = \delta Q - \delta E
$$

### Microscopic and Macroscopic Energy

$$
\Delta E = \Delta KE + \Delta PE + \delta U
$$

where:

* $\Delta KE$ is the change in kinetic energy;
* $\Delta PE$ is the change in potential energy;
* the change in the above two energies happens at the macroscopic scale, i.e. changes in KE and PE can be seen;
* $\Delta U$ is the change in internal energy; 
* the change in internal energy happens at the microscopic scale, i.e. changes in U cannot be seen.

### Energy Balance

$$
\dot{E}_{in} + \dot{E}_{gen} -|\dot{E}_{out}| = \dot{E}_{st}
$$

where:

* $\dot{E}_{in}$ is the rate of energy transfer in;
* $\dot{E}_{gen}$ is the rate of energy generated;
* $\dot{E}_{out}$ is the rate of energy transfer out;
* $\dot{E}_{st}$ is the rate of energy stored.

#### Surface Energy Balance
* No heat is generated or stored.

$$
\dot{E}_{in}-|\dot{E}_{out}| = 0
$$
