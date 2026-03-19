# 2026-01-30 Notes from S7 team digital twin (John's team)

Ominverse = VR / Digital twin env (Glorified Game Engine
Omniverse:
- Hard to work with
- good documentation
- bugs (a lot)

Point cloud - Lidar scan data (example)
# 2026-02-15 Agentic AI lookup

## Agentic AI
- Still and LLM like ChatGPT
- Task/action oriented LLM
- Independent, achieving specific goals with minimal human oversight
- AI that learns on itself by iterating the same task
- Still requires initial human input 
# 2026-02-18 Isaac Sim setup

## Isaac Setup
![[Isaac-Sim-UR5-Physics-Inspector.mp4]]
Creation of a scene with UR5 arm
- figured out how to move joints with **Physics Inspector**
- worked a bit with **Graph code** ("Block Coding")
![[Action-Graph-Isaac-Sim_v1.png|700x337]]
	- ros2 integration (some problems with setting the publisher)

# 2026-02-19 Github Hell

## Auth
- had to figure git and github authentication hell
- finally set up obsidian to git so i can make notes from different PCs
- useful for future work
# 2026-02-20 ros2 progress

## ros2 conn
confirmed properly connected ros2 to isaac-sim
- could send and set rviz timer to be the same as the isaac sim
- Still cannot control UR5 trough ros2


# 2026-02-24 Working on setting up the env (Isaac + Docker(ros2))

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


# 2026-02-27 Research focus


Recently I have shifted my focus on the research side of the project after conversations with my mentors regarding the approach of the assignment. It was obvious I was going head first into the development knowledge foundation. Therefore now my aim is to gather knowledge in the area and clearly define questions for my research based on the research gap that supposedly exists.

Currently the researched areas are: 
- Embodied AI - What exactly it is and how it works. 
	- [[Embodied AI(NVIDIA)|NVIDIA article]] explaining how one can be built and its use cases
- Agentic AI - What it is and how it works.
	- [[Agentic AI (by IBM)|IBM article]] that generally explains AgenAI and it's current and possible applications
- Connection between Embodied AI and Agentic AI
	- Are they the same? How are they connected etc.?
- Behavior trees - How do they work, difference with state machines, general understanding. 
	- Research paper that about LLM making behavior trees also explains concepts around the BTs very well

I have also set some technical research stuff like: 
- Isaac sim ticks and BT ticks. Can they be related and how? 


# 2026-03-02 Project plan

Today the main focus was building the project plan since I have stated in the meetings that I will do it with due date today. Submitted and waiting for reply. 


# 2026-03-04 Research progress

# AI and BT
Source: Robot Behavior-Tree-Based Task Generation with  Large Language Models

- Look into how a gen AI performs BT creation
- Creation from prompt-based learning

# ProgPrompt
Source: PROGPROMPT: Generating Situated Robot Task Plans  using Large Language Models

- Looked into the application of ProgPropmt and how it outperforms the general generation AI
- The importance of environmental awareness of the AI.


# 2026-03-06 End of week catch up

## End of front load research
- found enough materials to start the test bench development, also if i spend too much time I will slack behind.

## Documents
- asked for feedback on project plan, received from Gayatri, still waiting on Teade.
  
## Up next
- start with the development of workbench, set up all connections.



# 2026-03-09 Start of Workbench development

### MoveIt2 (ROS2 robitc manipulator)
- found a possible helper for the movement planner for the robot. Here can be defined start/end points and the planner moves the robot. Can useful for actions of the BT.
- Successful setup of MoveIt2 and planning of path. Can be useful to shorten development of the bench by not making my own planner and completing stuff, etc. I need to find a way to make the MoveIt2 receive outside parameters (as input from other node?) and to find a way to tie the MoveIt2 planning to the Isaac sim, so the planning can be visualized in isaac sim
  ![[MoveIt2-planning.mp4]]



# 2026-03-10 Preparation for sprint delivery, Bench development

## Sprint delivery
- small presentation laying out my current progress and next steps.
## MoveIt2 Nodes and topics
- trying to figure out the MoveIt2 Nodes and topics
- topics of the small node that sends position to MoveIt2![[rqt-tutorial-plus-hellomoveit.png]]
- 


# 2026-03-12 Company visit

## Revision of the meeting
- Still on bachelor level of approach, need to step it up
- Documentation of research needs to be made
- Looked trough the project plan
	- Too focused on technical development, too little research focus
	- No evidence of research 
	- Mention uncertainties, do not hide them.
This resulted in me starting to write down concrete plannings for each week so I do not hover around different topics and slow down. [[Planning]]



# 2026-03-13 Research BTs

- Read a survey paper about the BTs in general (Survey on BTs in robotics and AI).
- Looked into inconsistency where a site article states that BTs are not reactive, but BT reactive sequences exists. 


# 2026-03-16 Project plan and proper citation
Today I have been working on my study plan, organizing sources and citing them in the project plan document.  
Added proper performance measurement specifications and risk management table.

# 2026-03-18 Meetings and information gather
Today I had 3 meetings: 
- with Gayatri:
	We spoke about proper professional approach towards communication, meetings, and suggestions and approaches on writing project plans/research documentation
- with RobotLab:
	General meeting, shared progress with the rest of the team.
- with Teade:
	I've asked about information use cases, robot preference, etc. [[Meeting Notes Teade#2026-03-18 Technical specification - clarification]]  

# 2026-03-19 Looked into sim environments
Looked into sim environments based on the specifications and requirements. [[Simulation environment choice]]


