# Criteria
For the simulation environment I have set the following criteria:
- To be of industry standard (known, widely used in robotics development)
- Preferably native ROS2 connection (the less the set up the better)
- Easier learning curve - only forums can define this
- Preferably not tied to hardware... (like NVIDIA Isaac Sim)

Learning curve uses users experiences expressions from forums like reddit. Not concrete, but it is there. 

| **Sim Env**      | **ROS2 Connectivity**                        | **Learning curve** | **Hardware spec**               |
| ---------------- | -------------------------------------------- | ------------------ | ------------------------------- |
| Gazebo classic   | Native via gazebo_ros2_pkgs                  | Moderate​          | Standard CPU/GPU​               |
| Ignition Gazebo  | Native bridges and ros_control               | Moderate to steep  | Standard, low resource use      |
| Webots           | Official webots_ros2 package                 | Moderate           | Low to moderate                 |
| NVIDIA Isaac Sim | ROS2 Bridge extension                        | Steep              | High (RTX GPU, 32+GB RAM)       |
| CoppeliaSim      | ROS2 Interface plugin                        | Moderate           | Low resource use                |
| MuJoCo           | Via mujoco_ros2_control, ros2_control plugin | Moderate           | Low (CPU-focused, optional GPU) |
With all the information gathered till now, compelling choices are: Ignition Gazebo, Webots and Isaac sim. All of them provide provide good connectivity with ROS2 out of the box. Out of the tree I will go with Gazebo, since it has been most paired with ROS2, as well as low resource requirements and not being tied to hardware requirements.

Given that we are going with Ignition Gazebo and ROS2 on Ubuntu 24.04 LTS the following combination is needed for all connection to work:
- OS - Ubuntu 24.04 LTS (noble)
- Sim - Gazebo Harmonic LTS
- Framework/Middleware - ROS2 Jazzy LTS
These are the following requirements in terms of versions of software to have proper compatibility.



# Robot choice

1. [Tidy bot](https://tidybot2.github.io/) 
	Already built holonomic robot with 6 DOF, opens source
	Problem: mojuco only file found for now
2. Ridgeback + UR10
	Standard configuration, modeled in ROS2 using xacro 