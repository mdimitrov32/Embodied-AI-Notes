# General description 

Develop a demonstrator to transport well plates between robot lab nodes (e.g., pipetting robots, analysis devices) using robots such as Ufactory robotic arms, mobile AMRs, or AGVs. Build it in an Omniverse simulation to demonstrate the chain from GenAI/agentic AI to robot physics. The demonstrator uses behavior trees and ‘enriches’ these with world information using omnigraph. Specific situations will be considered in the demonstrator, like: docking of the mobile robot in front of the robot arm and handing over of well plates from arm to AMR/AGV.
For the demonstrator, an analysis will be added to indicate whether and how it could help the Fontys team's software development.


# Goals
## Development
- Develop a **minimal end-to-end pipeline**: an example is LLM → JSON plan → Behavior Tree → simulated robot execution.
- Gain familiarity with **simulation-based robotics**, ROS2, and Dockerized environments. Build and document the simulation infrastructure with high quality such that it can be the foundaiton of our research.
- Optionally integrate **basic perception** using simulator ground-truth and simple objects.
- Start the experimentation with Issac Sim.


## Research
- Explore **structured task planning** and agentic reasoning.
- Get an understanding of Progprompt, and foundation models for robotics.