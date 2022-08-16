
# PID Controler

**Basic (Plant) Form**
$$
\begin{equation}
    u(t) = K_p e(t)+K_I\int_0^t e(t)dt+K_D\dot e(t)
\end{equation}
$$

$K_p$ = Proportional gain
$K_I$ = integral gain
$K_D$ = dirivative gain

    Note: not all gains need to be used P, PD, PI are all valid.

## Linear Time Invariant Control

**Feedforward Control**

**Feedback Control**

**Transfer Function**
- models input to output in Laplace Domain
$$ 
\begin{equation}
    U(s) = G_cE(s) = (\frac{K_Ds^2+K_ps+K_I}s)E(s) 
\end{equation}
$$
- poles at origin = s
- zero at arbitrary places on complex plane
- PID selects PID for zeroes
- several popular algorithm for tuning PID like Zeigler-Nichols

        Multiplying by S in the Laplace domain is equivalent to taking a derivative in the time domain and 
        Dividing by S is equivalent to taking the integral.
        By adding these three terms of the PID controller together, we get a single transfer function for PID control


**Laplace domain**
- Laplace form makes it easier to determine the transfer function of the system
- Laplace transform gives a useful insight into understanding control performance

**Types of Controller Algorithms**
Simple
   - Lead-lag Controllers
   - PID Controllers
Complex
   - Nonlinear methods: Feedback Linearization, Backstepping, Sliding mode
   - Optimization methods: model predictive control

Dynamic System Model
- captures how the dynamic system reacts to outside force
  - comands, disturbances
- produces kinematics and dynamics 

Controller
- regulates the states of the vehical and outputs commands


System Representation
- plant system can be linear or non-linear
- plant representation: state-space form and transfer functions
- must be linear time-invariant