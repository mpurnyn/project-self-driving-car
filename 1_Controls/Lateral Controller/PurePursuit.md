# Pure Pursuit

## Geometric Path Tracking Controller
- any controller that tracks a path
- ignores forces acting
- assumes no-slip
- popular in robotics

Relies on a reference path ahead to follow

# Pure Pursuit
- wants to define a path that takes us from our current point to the next point.
- works in a manner similar to proportional control

$$

\delta = arctan(\frac{2Lsin\alpha}{K_{dd}v_f})

$$

**Crosstrack Error (Offset Error)** - the lateral distance between the heading vector and the target point.

**Heading error**
$$
\frac{-v(f)sin\delta(t)}{l} = \dot\psi_(t) 
$$

Heading and Crosstrack need to converge to zero 