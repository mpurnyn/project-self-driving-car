# Software Architectures
[Team VictorTango - DARPA Urban Challenge Technical Paper](https://pdfs.semanticscholar.org/c10a/cd8c64790f7d040ea6f01d7b26b1d9a442db.pdf)

## Software Decomposition
- describe the basic architecture of a typical self-driving software system
- no implementation details

one way to break it down
- environmental perception
  - uses sensors to mark environment elements like pedestrians, cars, bycycles, roadsigns
- environmental mapping
  - uses sensors and perception output to map environment
- motion planning
  - calculates a driving path using the perecption and mapping outputs
- controller
  - calculates the physical acutation of the car controlls to drive the path
- system supervisor
  - checks the states of all the modules.
  - informs the user


### Perception
localization
- gps/imu/wheel odometery
- determins vehical position

detecting dynamic object
    - lidar, cameras, radar
    - bounding boxes
    - object tracking 
    - object motion prediction
static object detection
    - uses hd road map to identify static objects

### Environmental Maps
occupancy grid
- uses object tracking and lidar
- outputs occupancy grid map

localization map
- uses object tracking and lidar to calculate a localization map

detailed road map
- uses pre-recorded data of road map, vehical position, segmented image, and static objects
- provides a detailed roadmap made up of segments/waypoints for the car to drive through


### Motion Planning
Decomposed into

Motion planner
- uses current goal, detailed roadmap, and vehicle position
- detemines the optimal sequence of road sements that connect origin to destination
- produces a mission path for behavior planner

Behavior planner
- uses current goal, detailed road map, vehical positon, dynamic objects, mission path
- solves short term planning problems
- calculates safe actions that can be taken along the mission path
  - i.e. should the veical merge
- outputs behavior constrainst

Local Planner
- occupancy grid, vehical position, dynamic objects, behavior constraint
- immediate or reactive planning
- must determine specific path and velocity pattern
- outputs trajectory


### Controller

Vehical Controller
- longitudinal control
- uses trajectory and vehicle position
- outputs trottle percentage and brake percentage

Steering Controller
- lateral control
- uses trajectory and vehicle position
- outputs steering angle


### Supervisor

Software Supervisor
- monitors the state of the components

Hardware Supervisor
- determins the health of the sensors
- checks if there is something unexpected blocking the sensors

