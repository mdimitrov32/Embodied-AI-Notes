# Building the mental string
## Hypothesis
- V1: AI has the potential to generate Behavior Trees that are functionally comparable to human-authored ones, though the conditions and limitations of this capability remain poorly understood.
  
- V2 (more concrete): AI has the potential to generate Behavior Trees that are functionally comparable to those authored by human experts for Autonomous Mobile Robot manipulators, though the conditions under which this capability holds and its limitations across task complexity, ~~environmental variability~~, and manipulation specificity, remain poorly understood.

## To say that the AI can make better BTs they need to be compared
**Claim:** To evaluate if the AI is capable of making a BTs that can be used in the field of robotics we need to evaluate the product made by it to the current standard (expert human making it). 

**Why?:** By evaluating the products from the two approaches, it can be determined if the AI is capable to produce BTs for the robotic industry. 

What is the evaluation metric? 

# Metrics
## Functional metrics
Functional metrics are metrics obtained trough observing the performance of the executioner of the BT (in this case - AMR manipulator) such as success/failure rate

The following metrics taken from the Evaluation BT paper: 
### Examples 
- Use of Resource - The metric is used to quantify the optimization of resource allocation, management, and utilization of its designated task. One example is the time it takes a BT to complete execution or time for single node execution. 
- Predictability Distance - This metric was originally defined by Colledanchise [15,19] for evaluating parallel behaviors. The approach consists of defining a target progress value and then calculating the average deviation between the expected and the actual time at which the action reaches progress closest to the desired value. While primarily utilized in the context of parallel behaviors, it can potentially be used in sequential behavior scenarios as well. (directly taken form paper, do not understand)
- Success Rate - Many definitions on success rate depending on context
	- Desired Behavior Success Rate - evaluates the extent to which the behavior executed by BT matches the expecting behavior from "behavior oracle"(whatever that means).  In safety accession a success might be the tree preferring avoidance of collision. For correctness, the success is the way/order a task is executed.
		- Defined by the ratio between the correct executions of the inner sub-behaviors over the total expected executions. If tree has 3 major nodes and one of them is for charging, we can evaluate the charging behavior, by evaluating the subtree behavior of that node. 
	- Single Node Success Rate - the ratio between the times the node has returned success vs the total executions of the node. refers to the ratio between the number of successful completions of a node n ∈ N (i.e., when it returns Success) and the total number of executions of the node, including both successful and failed attempts, denoted by $\huge{n_S}$ and $\huge{n_F}$ respectively. Mathematically, it is expressed as: $SR_n=\huge{\frac{n_S}{n_S+n_F}}$ 
- Unsafe state count - whenever a state leads to irreversible, undesired bahavior. Unsafe state count, measures the amount of unsafe states $U$ are encountered over the total states $T$ during the BT execution: $USC=\huge{\frac{^nU}{^nT}}$ The higher the $USC$  value the higher frequency of unsafe states. Does not correspond directly with success rate, it focuses on the identification and quantification of unsafe states. Can be complimentary safety metric. 
- Condition check frequency - quantifies the frequency at which a specific condition node is ticked/evaluated over a given time: $CFF=\huge{\frac{n\_evaluations}{\Delta T}}$ where $n\_evaluations$ is the number of times a the condition node is ticked and $\Delta T$ is the time interval. Higher $CFF$ indicates higher check frequency. Can be used for BT reactivity. 
## Non-functional metrics
Non-functional metrics are the metrics of the static properties of the BT, such as tree depth, condition-to-fallback ratio, action granularity, etc. Anything that is inside the behavior tree after creation.


# Disclaimer 
The [Metrics](Behavior tree evaluation#Metrics) part is majorly copied or paraphrased from the *Evaluation behavior trees* paper and does not contain new information or research from my side. It is solely written for understanding of the paper and its contents, as well help in the future of my research.  

