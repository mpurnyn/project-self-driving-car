# project-self-driving-car


# Link to starting template and simulator
https://d3c33hcgiwev3.cloudfront.net/ZQFoJyNEEem3Cw5hhdQCGg_65256a90234411e982bdbb99b90531e3_Course1FinalProject.zip?Expires=1663027200&Signature=lElJvGnSwPpRyqkx~sToOLImsozc3bsBio6ImykxEfsfZ4csEfeZh4Pl9cC3TdxYLRoSZ~43eL24A7by6iHNiHoys5znvbe-PGD3-ugJ3fVtVmo2ca7KcU-ktBSnwetsg~ZpMRpijKt2nNd59VYYxKjsRB1~AVipUB8N4xmw8dY_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A



The "controller2d.py" file contains a controller object. 


- update_controls method 
- find all comment blocks that contain "MODULE 7"
- output: vehicle throttle, steer, and brake.

- All units are in SI (meters, seconds, radians), and 
- CARLA works in the left-handed coordinate system 
- (due to the Unreal Engine adopting the left-handed coordinate system). This generally shouldn't be an issue for this assignment since the controller operates in the x, y and yaw space.


- waypoints[2][1]
- More details on the structure of the waypoint variable is written in the comments of the controller2d.py file.

waypoints are a linearly interpolated (for location and speed) subset of the entire set of waypoints 
(from racetrack_waypoints.txt).


you will output vehicle throttle, steer, and brake.


inputs

pose: x,y,yaw
speed: v
time: t
desired speed v_desired
waypoints[i][x,y,v]


outputs

throttle 0 to 1
steer output -1.22 to 1.22
brake_output 0 to 1


