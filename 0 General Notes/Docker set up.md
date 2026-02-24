#docker 

>[!warning]
Install the Docker-Engine (CLI) and **NOT** Docker Desktop!!! Docker Desktop runs in a **VM** which causes a lot issues down the road...

Helpful [[Docker helpful commands|commands]] for docker.

ros2 image: **ros2 jazzy desktop**
```
docker pull osrf/ros:jazzy-desktop
```

### ROS2 on Docker with host connection and display

ROS2 on Docker has to have connections to your host machine to utilize host network, display, etc. If rviz and/or host connection is needed to host the following container creation works:
```
docker run -it \
  --name ros2jazzy \
  --net=host \
  --ipc=host --pid=host \
  --env="DISPLAY=$DISPLAY" \
  --env="QT_X11_NO_MITSHM=1" \
  --env="ROS_DOMAIN_ID=0" \
  -v /tmp/.X11-unix:/tmp/.X11-unix:rw \
  -v $XAUTHORITY:/root/.Xauthority \
  osrf/ros:jazzy-desktop
  tail -f /dev/null
```
This command creates a container that has connection to hosts network and display allowing for rviz to work properly

#  ==TO FIX (some of this work but train of thought is off)==
==run secondary terminal in the same container:
```
# On host, in another terminal:
docker exec -it ros2jazzy bash
```
Then source the ros2. "exec" does not go trough the entry point (/ros_entrypoint.sh)
sourcing:
```
source /opt/ros/jazzy/setup.bash
```
Check if thhe docked ROS2 has **ROS_DOMAIN_ID** with:
```
echo $ROS_DOMAIN_ID
```
If it returns blank output change it to "0" and relaunch rviz (or docker to be sure): 
```
export ROS_DOMAIN_ID=0
```
==
