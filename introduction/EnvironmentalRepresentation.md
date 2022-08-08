# Environmental Representation

## Localization Map (Point Cloud Map or Feature Map)
- continuous collection of data and updating
- difference between current and previous map is used to calculate the movement
- important for planning a path

## Occupancy Grid
- avoid colision with static objects
- 2d or 3d map
- discrete, fine grain grid
- occupied cells are non-drivable areas
  - before detemining the static objects you need to remove
    - the dynamic objects
    - the non-interfereing static objects.
- this is probablistic so only gives a rough idea and you cant blindly trust it
- more detailed scans are needed to determin objects.
  
## Detailed Road Map
used for planning mission plan
- made of road segments, lane boudaries, traffic regulation (like traffic lights)

can be created
- fully online
- fully offline
- created offline then updated online

Can be stored with the "lanelet" model

[P. Bender, J. Ziegler and C. Stiller, "Lanelets: Efficient map representation for autonomous driving," 2014 IEEE Intelligent Vehicles Symposium Proceedings, Dearborn, MI, 2014, pp. 420-425. doi: 10.1109/IVS.2014.6856487 (Lanelet)](https://ieeexplore.ieee.org/abstract/document/6856487)