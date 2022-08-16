# PID + Feed Forward

## Feed Back (PID)
- Closed Loop
- takes previous output into consideration.
- reactive response

feedback controller generates the actuator signal u_fb based on velocity error

## Feed Forward
- Open Loop
- Feed Forward to Plant  produces output
- predictive response
- 
**Look-up Table**
Feedforward generates actuator signal u_ff based on the predefined lookup table. 
- This lookup table allows us to generate a Throttle angle based on the Engine RPM and the Torque Needed.
- Assumes vehicle is at steady state.

wheel_rpm = reference/relationship
engine_rpm = wheel_rpm / Gear Ratio

engine_torque = total_load_torque
- calculated by vehical speed and slope
- affected by rolling resistance, aerodynamic resistance, and gravity force
engine_torque = v - r_resistance  
$$
\begin{align}
    Torque =
    F_{load} &= F_{aero} + R_x + F_g \\
    F_{aero} &= \frac{1}{2} C_a \rho A \dot{x}^2 = c_a \dot{x}^2\\
    R_x &= N(\hat{c}_{r,0} + \hat{c}_{r,1}|\dot{x}| + \hat{c}_{r,2}\dot{x}^2) \approx c_{r,1} \dot{x}\\
    F_g &= mg\sin{\alpha}
\end{align}
$$

## Feeback + Feed Forward
Feedfoward is used for predictive response, non-zero offeset
Feedback is used to correct the response and compensate for **disurbances** and **errors**
    
    Note: because Feedback needs errors to exist before it can correct them it lags behind the FeedForward


## Equations
Feeback(reference - actual) + FeedForward(reference) = Actual

### References

[Sailan, K., Kuhnert, K.D., "Modeling and Design of Cruise Control System with Feedforward For All Terrain Vehicles", Computer Science & Information Technology (CS & IT). 2013.](https://airccj.org/csecfp/library/Search.php?title%3DMODELING%2BAND%2BDESIGN%2BOF%2BCRUISE%2BCONTROL%2BSYSTEM)