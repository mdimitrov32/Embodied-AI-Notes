# Building the mental string
## Hypothesis
- V1: AI has the potential to generate Behavior Trees that are functionally comparable to human-authored ones, though the conditions and limitations of this capability remain poorly understood.
  
- V2 (more concrete): AI has the potential to generate Behavior Trees that are functionally comparable to those authored by human experts for Autonomous Mobile Robot manipulators, though the conditions under which this capability holds and its limitations across task complexity, ~~environmental variability~~, and manipulation specificity, remain poorly understood.

## To say that the AI can make better BTs they need to be compared
**Claim:** To evaluate if the AI is capable of making a BTs that can be used in the field of robotics we need to evaluate the product made by it to the current standard (expert human making it). 

**Why?:** By evaluating the products from the two approaches, it can be determined if the AI is capable to produce BTs for the robotic industry. 

What is the evaluation metric? 
## Functional metrics
Functional metrics are metrics obtained trough observing the performance of the executioner of the BT (in this case - AMR manipulator) such as success/failure rate, amount of fallbacks, etc. Anything that can be obtained during runtime.

## Non-functional metrics
Non-functional metrics are the metrics of the static properties of the BT, such as tree depth, condition-to-fallback ratio, action granularity, etc. Anything that is inside the behavior tree after creation.


