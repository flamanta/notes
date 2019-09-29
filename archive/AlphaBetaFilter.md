# Alpha Beta Filter

* Also known as the g-h filter<br>
<br>
* $g$ is the scaling used for measurement (also known as $\alpha$)
* $h$ is the scaling for the change in measurement over time (also known as $\beta$) <br>
<br>
* Basis for a huge number of filters including the Kalman filter
* Each type of filter has a different way of assigning values to $g$ and $h$
* Kalman filter varies $g$ and $h$ dynamically at each time step<br>

## Formal Terminology

* *System/plant*: the object we want to estimate
* *State*: actual **hidden** value of system 
* *Measurement*: measured, **observable** value of system
* *(State) estimate*: filter's estimate of state
* *Process/system model*: mathematical model of the system
* *Process/system error*: error in mathematical model of the system
* *System propogation/evolution*: uses process model to form new state estimate; imperfect because of process error<br>

## Algorithm

<b>Initialization</b>
<pre><code>1. Initialize the state of the filter
2. Initialize our belief in the state
</code></pre>
<b>Predict</b>
<pre><code>1. Use system behavior to predict state at next time step
2. adjust belief to account for uncertainty in prediction
</code></pre>
<b>Update</b>
<pre><code>1. Get measurement and associated belief about its accuracy
2. Compute residual between estimated state and measurement
3. New estimate is somewhere on residual line
</code></pre>

## Notation

* $z$: measurement (some literature uses $y$)
* $k$: time step
* $z_{k}$ is the measurement for time step $k$ <br>
<br>
* In general, we have n sensors and n measurements
* **x** denotes the state; represents both initial weight and initial weight gain rate
* $\dot{x}$ is the derivative of x with respect to time
$$
\mathbf{x} = 
\begin{bmatrix}
x \\
\dot{x}
\end{bmatrix}
$$
* e.g weight of 62 kg with a gain of 0.3 kg/day
$$
\mathbf{x} =
\begin{bmatrix}
62\\
0.3
\end{bmatrix}
$$
<br>
* The state is initialized with $x_{0}$, the initial estimate.
* We then enter a loop, predicting the state for time or step $k$ from the values from time or step $k-1$.
* We get the measurement $z_{k}$ and choose intermediate point between measurements and prediction, creating the estimate $x_{k}$