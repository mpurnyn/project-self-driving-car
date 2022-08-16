# Bicycle Kinematics
- useful for understanding the bascis of dynamic kinematics

## Model Boundaries
- The bicycle begins with zero v and angle, 
- it has a maximum turning rate of 1.22 rad/s,
- the wheelbase has a length of 2m
  - with length of 1.2m to the center of mass from the rear axle.

## Velocity X and Y Component Equations
$$
\begin{align*}
dx_c &= v \cos{(\theta + \beta)} \\
dy_c &= v \sin{(\theta + \beta)} \\
\end{align*}
$$

## Angle (Heading) Calculations
$$
\begin{align*}
d\theta &= \frac{v \cos{\beta} \tan{\delta}}{L} \\
d\delta &= \omega \\
\beta &= \tan^{-1}(\frac{l_r \tan{\delta}}{L})
\end{align*}
$$

- The input can also directly be the steering angle $\delta$ rather than its rate in the simplified case.




