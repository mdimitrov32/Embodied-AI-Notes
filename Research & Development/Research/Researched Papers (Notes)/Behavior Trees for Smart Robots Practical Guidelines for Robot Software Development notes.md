
Bridges the gap between fundamental research and practical application of BT for autonomous robots. 

Contains general BT explanation, like node types and usage

> [!Info]  Decorator Node
> Modifies the execution of its child node (it is only one), like invert, timeout, or repeat until success

Fall back nodes are used for prioritized alternative that leads to the same postcondition. 

BT are not easily verifiable  

BT creation plan:
(1) Describe context and purpose of the robot.
- helps identify tasks for the robot
- c4model
(2) Basic plan—describe a “good weather” BT. 
(3) Create a robust plan. 
(4) Add reactivity to the plan.