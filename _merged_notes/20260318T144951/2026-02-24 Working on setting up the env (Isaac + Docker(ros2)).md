
## Dockerized ROS2 jazzy

- Successful set up of ros2 within Docker with the ability to use the host network and display (for rviz2)
  ![[ros2-docker-rviz2.png]]

- managed to create a publisher on the isaac sim to publish sim time
  ![[isaac-sim-time-publisher.png]]
- Attempts to read the isaac time form the dockerized ros2 rviz2 - unsuccessful. 
  - issues with host network usage - resolved trough allowing the connection to host network
  - issues with rviz2 not finding display/cant start - resolved trough passing the host environments 
  - ==docked ros2 is able to see the topic from ros2 but not read it - unresolved. Issue might lie in the way docker wants to communicate NEED HELP.== 
	  - Possible solving issue - everything in a docker (isaac sim + ros2)