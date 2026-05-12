**Instructions** - A set of general instructions to set up the AI behavior, like "only give XML", "compatible with BTCPP v4", "use only provided data", etc.

**Input** - The core text of the prompt, text explanation of the robot type, task and execution. Here can go the specification of the task hierarchy if any, specify if you want certain actions to be reactive, if you have BT design in mind, etc. Prompt the LLM to use your predefined Actions and conditions, explanation if needed.

**Actions, Condition, Data** - Specify your created leaf nodes of actions and condition checks, and any type of data that goes into a leaf node, for example MoveTo(position) and include list of positions available for LLM to pick.


### Instructions (Taken example form BTGenBot-2):
You are helpful assistant that can assist with creating behavior trees. Your task:
- Convert provided summary of behavior into XML-formatted behavior tree.
- Ensure the behavior tree matches the description in the summary
- The behavior tree must be compatible with the BehaviorTree.CPP library.
- Only use the actions and parameters provided in action list below the summary.

Output Requirements:
- Output only the XML representation of the behavior tree. Do not include explanation, comments, or any additional text. 
- Ensure all actions and parameters strictly match the provided list.
- If possible limit the use of SubTrees

### Input (structure taken from BTGenBot-2, adjusted for current research):
The behavior tree facilitates a robot's navigation and manipulation by implementing a fallback mechanism to achieve its tasks. The robot has 2 main task of same importance and execution and reactive behavior for low battery and charging. For the robot to accomplish the task it has to move between 6 available locations, pick and place 2 identical objects in the same manner, from their available location to pick to their designated place location. The robot possesses available actions and condition nodes to check what is holding and what is available to pick. It is of huge importance for the robot to be able to continue pick and place tasks even when interrupted due to low battery.

ACTIONS

MoveTo — moves robot to a location
  location      (str, required)    target location
  running_ticks (int, default 3)   travel time in ticks

Pick — picks a named object at current position
  object_name   (str, required)    object to pick
  running_ticks (int, default 2)   pick time in ticks

Place — places currently held object
  object_name   (str, required)    object expected to be held
  running_ticks (int, default 2)   place time in ticks

Charge — charges battery, must be at charger position
  running_ticks (int, default 5)   charge time in ticks
  charge_to     (int, default 100) target battery level


CONDITIONS

BatteryAboveCheck — checks if battery is above threshold
  threshold        (int, default 20)   minimum battery %

AtPosition — checks if robot is at a location
  location         (str, required)     location to check

ItemAvailable — checks if a named object is available
  object_name      (str, required)     object to check
  require_location (str, default None) if set

IsHolding — checks if robot is holding an object
  object_name      (str, default None) if None, checks if holding anything


LOCATIONS
Locations.BASE      base position
Locations.CHARGER   charger position
Locations.PICK_A    pick location for item A
Locations.PLACE_A   place location for item A
Locations.PICK_B    pick location for item B
Locations.PLACE_B   place location for item B


OBJECT NAMES
"A"   item A
"B"   item B


All nodes require name (str) and state (dict) as first two arguments.


