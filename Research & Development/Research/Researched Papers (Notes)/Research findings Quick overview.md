
# BT creation options

![[Meeting board#^frame=BoardFrame|90%]]
![[LLM-as-BT-Planner-getTypes.png]]

Many options already exist:
- single run generation - said **"generate BTs directly for an assembly subgoal coming from the upstream module"** I understand it as: The designated goal (action goal) is given as final execution node. Internal LLM iteration till it fits the requirement. 
- iterative with BT simulation to confirm when the BT returns SUCCESS eventually. Essentially tell LLM to create BT and run it if it works.
-  Human-in-loop: A human-AI communication till human gives green light, on failure goes back to AI








