
Bridges the gap between fundamental research and practical application of BT for autonomous robots. 

Contains general BT explanation, like node types and usage

> [!Info]  Decorator Node
> Modifies the execution of its child node (it is only one), like invert, timeout, or repeat until success

Fall back nodes are used for prioritized alternative that leads to the same postcondition. 

BT are not easily verifiable  

BT creation plan:
(1) Describe context and purpose of the robot.
- helps identify tasks for the robot
- c4modelss
- identify major actions
- think about non functional requirements, like battery, inaccessible location, etc. 
- think about scenarios, edge cases? 
- think of robot states - state can be robot position in world. 
(2) Basic plan—describe a “good weather” BT. 
- first BT draw should be in perfect conditions 
- after that take into consideration outside disturbances 
(3) Create a robust plan. 
- Robust Logical-Dynamical Chain
(4) Add reactivity to the plan.
- handling contingencies asap (placed on the left from deliberate subtree)
- 