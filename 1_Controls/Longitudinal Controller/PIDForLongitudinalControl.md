# PID Controller for Longitudinal Control

## Example: Cruise Control 
- keep the speed at a reference speed

### Plant Vehical Model
- Input - Reference Velocity
- Reference Value to Achieve - Vehical Velocity
- Output - Acceleration

The model is split into two controllers
####  High Level 
- calculates acceleration to reached needed velocity




#### Low Level 
- calculates the throttle/brake input needed to achieve the acceleration necessary to achieve the desired veloctiy

Assumptions 
- that only throttle is necessary
- driver will use brake
- gear is fixed at 1:1

1. Converts the Desired Acceleration to a Torque needed
$$
\begin{align}
    T_e = \frac{J_e}{(GR)(r_{eff})}a + T_{load} 
\end{align} 
$$
2. Use the Steady-State map of RPM and Torque to Throttle Angle convertion.

       Note the engine map non-linearity can cause some artifacts in the resulting Throttle Angle (it wont be smooth).

       Gear Changes can cause challenges for pure PID Control.
       
[Chapter 5 (pp. 123-150) of R. Rajamani, "Introduction to Longitudinal Control " In: Vehicle Dynamics and Control, Mechanical Engineering Series](https://www.springer.com/cda/content/document/cda_downloaddocument/9781461414322-c1.pdf?SGWID%3D0-0-45-1265143-p174267791)