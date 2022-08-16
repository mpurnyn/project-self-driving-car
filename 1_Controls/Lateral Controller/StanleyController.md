# Stanley Controller
- geometric path tracking
- stability proof - no matter the conditions it will drive the car to the path
- doesnt account for noisy velocity estimates
## Approach

- Uses the center of the front axle
- Looks at 
  - the error in the heading and 
  - the error in the position relative to the closest point on the path
- Define an intuitive steering law
  - correct heading error
  - correct position 
  - obey max steering angle bounds

### Combine 3 Components

#### correct heading error
Steer to align heading with desired heading
$$
\delta(t) = \psi(t)
$$

#### correct position
Steer to eliminate crosstrack error
    - proportional to error
    - inversely proportional to speed
    - limit effect for large errors with inverse tan
    - gain k determined experimentally.
$$
\delta(t) = arctan(\frac{ke(t)}{v_f(t)})
$$

#### Maximum and minimum steering angles
$$
\delta(t) \in [min,max]
$$

## Cross Track Error

$$

$$


## Adjustments to Stanley
It is good for getting on the path and has high stability, but the ride and turns may be too harsh for a rider.

### Low Speed Operation Fix
- inverse speed can cause numerical instability
- add a "softening constant" to controller
$$
\delta(t) = arctan(\frac{ke(t)}{k_{softening}+v_f(t)})
$$

### Extra Dampening on heading
- becomes an issue at higher speeds in a real vehicle
### Steer into constant radius curves
- Improves tracking on curves by adding a feedforward term on heading