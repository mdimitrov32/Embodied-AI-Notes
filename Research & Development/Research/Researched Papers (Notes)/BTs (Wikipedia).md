Source: https://en.wikipedia.org/wiki/Behavior_tree_(artificial_intelligence,_robotics_and_control)

# 1. General Explanation
## Key concepts

- Root Node
	No parent, one child
- Control Flow
	- One parent, at least one child
	- Control flow nodes can be selectors (fallback) or sequence nodes
		- Fallback nodes - executes the first child that does not fail, Immediately returns success or running when one of the children returns success or running. Children are ticket in order of importance from left to right.
		- Sequence nodes - will return failed or running immediately after one of the children returns  failure or running
- Execution Node
	One parent, no children



