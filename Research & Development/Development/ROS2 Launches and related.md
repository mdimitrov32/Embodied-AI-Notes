# Gazebo launch from ros
```ros2 launch ros_gz_sim gz_sim.launch.py```
# clearpath r100 setup
https://docs.clearpathrobotics.com/docs/ros/tutorials/simulator/install/
https://docs.clearpathrobotics.com/docs/ros/tutorials/simulator/simulate
-  Launch sim with 
```
ros2 launch clearpath_gz simulation.launch.py rviz:=true
```
 add ```world:=<world_name>``` to change world


- Launch teleop with ```
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=true -r __ns:=/r100_0000
```


# MoveIt launch command

```
ros2 launch clearpath_manipulators moveit.launch.py \
  setup_path:=$HOME/clearpath \
  use_sim_time:=true

ros2 launch clearpath_viz view_moveit.launch.py \
  namespace:=r100_0000 \
  use_sim_time:=True
```


This is the Gazebo sim:
```
# Terminal 1
ros2 launch clearpath_gz simulation.launch.py setup_path:=$HOME/clearpath
```

The MoveIt planner
```
# Terminal 2 (after Gazebo is up and you've hit play)
ros2 launch clearpath_manipulators moveit.launch.py setup_path:=$HOME/clearpath use_sim_time:=true
```

Moveit Viz
```
# Terminal 3
ros2 launch clearpath_viz view_moveit.launch.py namespace:=r100_0000 use_sim_time:=True
```