# Gazebo launch from ros
```ros2 launch ros_gz_sim gz_sim.launch.py```
# clearpath r100 setup
https://docs.clearpathrobotics.com/docs/ros/tutorials/simulator/install/
https://docs.clearpathrobotics.com/docs/ros/tutorials/simulator/simulate
-  Launch sim with ```ros2 launch clearpath_gz simulation.launch.py rviz:=true```
	- add ```world:=<world_name>``` to change world

- Launch teleop with ```ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=true -r __ns:=/r100_0000```
	- 

