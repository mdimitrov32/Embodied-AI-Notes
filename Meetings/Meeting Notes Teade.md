
# 2026-02-04 Project Plan review 

## Research questions
Refine the idea behind the research questions.
Give context to the questions.

How does the Agentic AI maps to BT?


Add to Project Plan:
State what I want to do in the future weeks.

How to implement Agentic AI in robot context? General 
How to apply AgenAI in BT?
Can i replace BT whit AgenAI or integrate it?

Define questions for Single responsibility.
Readjust questions order: start with BT related and then AI. 

Context: we know about BT in robotics

We talk about the brain (high level) action selection.

We should think about in the context of the RobotLab

Questions: How does fully AgenAI robotic controls performs compared to BT? 

%% What happens if the AgenticAI makes wrong assumptions?  %%

In case of Agen outperforms BT: Whow can we improve BTs with the better performance of Agen?

In case of Agen underperform: 

What If we just combine them Agen + BT? What if we take the best of bot worlds? 

BT is better explainable and AI is faster working. 

End Products:

- Test Bench: A platform for conducting the experiments. 
- Code: A proof of concept on the topic.
- Document: A report detailing the findings during the research.


# 2026-02-25 1-on-1 Meeting 

## Stuff to look at 
- Check sim frequency change ^simFreq
- IS (Information system) 
- Tick in a BT - is it similar as in the Isaac Sim. 


## Questions for research (possible):
What amount of guard rails does AI need in behavior trees? Safety related
Which parts of the BT should be allowed to set/used by AI?
Letting AI Agent free vs containing it with guardrails? 

Clear view on EmbodiedAI and AgenticAI? Are they related, if yes, how?
Embodied AI - What it is? 
- What the rest have done? Where they have succeeded and failed? How to accomplish and how to prevent? 


## Agentic AI explained:
- Many small agents managed by bigger one

## Environment settings
- The environment for now remains on the host and at later stage can be dockerized. There is no need for additional complications at the current stage.

# 2026-03-18 Technical specification - clarification and more

What specific actions does the AMR need to do for the research?
- Move to nodes (stations), do arm actions.  
- the idea is to move in between non close
- Look into safety actions. 

BT examples that have been made? search for examples on AMR

The Construct - online sim for robotics.
(Andy) Cooper's Lab - robots in labs.


Ask for use cases Mark Becks(start here), Mark Driver(maybe later).


What are example AMRs to use for the simulation?
AGV/AMR - Gecko Afular
Look into both frameworks for robot control. 

tank based - no turning

triangular shapes - holonomic - preferred
50cm footprint

OpenTCS - look into that, open source tool


look for model simulation environments
- look for ROS2 connectivity
- Easiness of usage

Speak with student in TQ (Mark Becks)

Vladislav - TQ 5.2 Smart system labs

For the next week: 
- sim env for ROS2 ease of use and general ease of use (Research)
- discuss if stuck 

# 2026-03-25 Meeting (with Peter)

Give version to the project plan 

Add research question. 
Search for known examples that have been investigated for BTs. I have to compare with exciting examples of BTs. 

Explore why would a AI generated BTs is better than Humanly-made.

Reproducible behavior from AI agent.

Go first for the available stuff (AI and human) and then go for the hybrid later. 

Explorative approach look into all of them.

If I say something (the What?) I have to explain the Why? 

Provide pictures for clearer understanding 

How can Agentic AI do BTs




