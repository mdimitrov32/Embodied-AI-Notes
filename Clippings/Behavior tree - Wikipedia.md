---
title: "Behavior tree - Wikipedia"
source: "https://en.wikipedia.org/wiki/Behavior_tree"
author:
  - "[[Contributors to Wikimedia projects]]"
published: 2009-01-28
created: 2026-02-23
description:
tags:
  - "clippings"
---
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/88/Building_a_System_Out_of_its_Requirements.png/500px-Building_a_System_Out_of_its_Requirements.png)

Building a system out of its requirements – dynamic view

![](https://upload.wikimedia.org/wikipedia/en/thumb/0/05/Static_Integrated_View.jpg/500px-Static_Integrated_View.jpg)

Building a system out of its requirements – static view

A **behavior tree** is a structured visual [modeling](https://en.wikipedia.org/wiki/Modeling "Modeling") technique used in [systems engineering](https://en.wikipedia.org/wiki/Systems_engineering "Systems engineering") and [software engineering](https://en.wikipedia.org/wiki/Software_engineering "Software engineering") to represent system behavior. It utilizes a hierarchical tree diagram composed of [nodes](https://en.wikipedia.org/wiki/Node_\(computer_science\) "Node (computer science)") and connectors to illustrate [control flow](https://en.wikipedia.org/wiki/Control_flow "Control flow") and system actions. By replacing ambiguous [natural language](https://en.wikipedia.org/wiki/Natural_language "Natural language") descriptions with standardized visual elements—such as boxes, arrows, and standard symbols—behavior trees improve clarity, reduce misinterpretation, and enhance understanding of complex systems.[^1]

## Overview

The extensive amount of detail involved in describing the numerous requirements of a large-scale system using natural language can lead to [short-term memory](https://en.wikipedia.org/wiki/Short-term_memory "Short-term memory") overload,[^2] [^3] hindering a comprehensive understanding of the system's needs.[^4] [Natural language](https://en.wikipedia.org/wiki/Natural_language "Natural language") often introduces ambiguities, aliases, inconsistencies, redundancies, and incomplete information to concepts.[^5] This creates uncertainty and over-complicates systems.

The behavior tree representation attempts to eliminate uncertainty by limiting vocabulary to the original requirements. Large requirement sets may require the help of a composition tree [^6] representation that resolves aliases and other vocabulary problems in a prior step. The aim is to produce a deep, accurate, and holistic representation of system needs [^2] that can be understood by all readers (often [stakeholders](https://en.wikipedia.org/wiki/Project_stakeholder "Project stakeholder")). Since the behavior tree notation uses [formal semantics](https://en.wikipedia.org/wiki/Semantics_of_programming_languages "Semantics of programming languages"), it can serve as input for further processing, such as making an [executable](https://en.wikipedia.org/wiki/Executable "Executable") for a given set of requirements.

![](https://upload.wikimedia.org/wikipedia/en/thumb/7/7f/Set_of_Requirements_Behavior_Trees.jpg/500px-Set_of_Requirements_Behavior_Trees.jpg)

Set of four requirements behavior trees

![](https://upload.wikimedia.org/wikipedia/en/thumb/e/ec/Requirements_Integration_Process.jpg/500px-Requirements_Integration_Process.jpg)

Requirements Integration Process

Both single and integrated (composite) behavior tree forms are important in applying behavior trees in [systems](https://en.wikipedia.org/wiki/Systems_engineering "Systems engineering") and [software engineering](https://en.wikipedia.org/wiki/Software_engineering "Software engineering").

- **Requirement behavior trees (RBT):** Initially, individual requirement behavior trees are constructed to capture all behavioral fragments from each natural language requirement, using a rigorous translation process that preserves both intent and vocabulary. The translation process can uncover a range of defects in original [natural language](https://en.wikipedia.org/wiki/Natural_language "Natural language") requirements.
- **Integrated behavior trees (IBT):** Because a set of requirements imply the integrated behavior of a system, all the individual requirement behavior trees can be composed to construct an integrated behavior tree that provides a single holistic view of the emergent integrated behavior of the system. This enables the construction of the system's integrated behavior from its requirements.[^7] An analogy to help describe this process is the transition from a randomly arranged set of [jigsaw puzzle](https://en.wikipedia.org/wiki/Jigsaw_puzzle "Jigsaw puzzle") pieces to putting each of the pieces in its appropriate place. When this happens, each piece of information is placed in its intended context and their collective emergent properties become clear.

Having all the requirements converted to behavior trees (RBT) is similar to having all the pieces for a [jigsaw puzzle](https://en.wikipedia.org/wiki/Jigsaw_puzzle "Jigsaw puzzle") randomly spread out on a table – until all the pieces are connected, the emergent picture remains unclear, and it is uncertain whether any pieces are missing or don’t fit. Constructing an integrated behavior tree (IBT) reveals emergent behavior and missing pieces.[^8] [^5]

Critical aspects of behavior engineering representation and process are listed below.

**Representation:**

- The composition tree's role in the overall process is to provide a means to overcome the imperfect knowledge associated with the large set of requirements for a system.

**Process:**

- Behavior engineering uses behavior trees to control complexity while growing a shared understanding of a complex system.
- A shared holistic understanding of a complex system integrates requirements to show its implied emergent behavior.

## History

Behavior trees and the concepts for their application in [systems](https://en.wikipedia.org/wiki/Systems_engineering "Systems engineering") and [software engineering](https://en.wikipedia.org/wiki/Software_engineering "Software engineering") were originally developed by Geoff Dromey.[^8] [^5] [^9] [^10] The first publication of some of the key ideas were in 2001.[^11] Early publications on this work used the terms "genetic software engineering" and "genetic design" to describe the application of behavior trees. The reason for originally using the word "genetic" was because sets of genes, sets of jigsaw puzzle pieces, and sets of requirements, when represented as behavior trees, all appear to share several key properties:

- They contained enough information as a set to allow them to be composed – with behavior trees, this allows a system to be built out of its requirements.
- The order in which the pieces were put together was not important – with requirements, this aids in coping with complexity.
- When all the members of the set were put together, the resulting integrated entity exhibited a set of important [emergent properties](https://en.wikipedia.org/wiki/Emergent_properties "Emergent properties").

For behavior trees, important emergent properties include:

- The integrated behavior of the system is implied by the requirements.
- The coherent behavior of each component is referred to in the requirements.

These genetic parallels, in another context, were originally spelled out by Adrian Woolfson.[^12] [^13]

Despite these legitimate genetic parallels, it was felt that this emphasis led to confusion with the concept of [genetic algorithms](https://en.wikipedia.org/wiki/Genetic_algorithms "Genetic algorithms"). As a result, the term behavior engineering was introduced to describe the processes that exploit behavior trees to construct systems.

Since the behavior tree notation was originally conceived, several people from the Dependable Complex Computer-based Systems Group (DCCS – a joint [University of Queensland](https://en.wikipedia.org/wiki/University_of_Queensland "University of Queensland"), [Griffith University](https://en.wikipedia.org/wiki/Griffith_University "Griffith University") research group) have made important contributions to the evolution and refinement of the behavior tree notation and usage.[^14]

Probabilistic timed behavior trees have been developed by researchers such as Rob Colvin, Lars Grunske, and Kirsten Winter of the DCCS, so that reliability, performance, and other [dependability](https://en.wikipedia.org/wiki/Dependability "Dependability") properties could be expressed.[^15]

## Key concepts

![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Core_Elements_of_the_Behavior_Tree_Notation.png/960px-Core_Elements_of_the_Behavior_Tree_Notation.png)

Core elements of the behavior tree notation

A behavior tree is used to formally represent the *fragment of behavior* in each requirement. In general, behavior for a large-scale system, where [concurrency](https://en.wikipedia.org/wiki/Concurrency_\(computer_science\) "Concurrency (computer science)") is admitted, appears abstractly as a set of [communicating sequential processes](https://en.wikipedia.org/wiki/Communicating_sequential_processes "Communicating sequential processes"). The behavior tree notation captures these composed component-states and represents them as a tree-like form.

Traceability tags (see Section 1.2 of behavior tree notation) in behavior tree nodes link the formal representation to the corresponding [natural language](https://en.wikipedia.org/wiki/Natural_language "Natural language") requirement.[^16]

A behavior tree with leaf nodes may revert (symbolized by adding the [caret](https://en.wikipedia.org/wiki/Caret "Caret") operator "^") to an ancestor node to repeat behavior or start a new thread (symbolized by two carets "^^").

For a complete reference to behavior tree notation, see *Behavior Tree Notation v1.0* (2007).

### Semantics

The [formal semantics](https://en.wikipedia.org/wiki/Semantics_of_programming_languages "Semantics of programming languages") of behavior trees is given via a [process algebra](https://en.wikipedia.org/wiki/Process_algebra "Process algebra") and its [operational semantics](https://en.wikipedia.org/wiki/Operational_semantics "Operational semantics").[^17] The semantics have been used as the basis for developing [simulation](https://en.wikipedia.org/wiki/Simulation "Simulation"), [model checking](https://en.wikipedia.org/wiki/Model_checking "Model checking"), and [failure modes and effects analysis](https://en.wikipedia.org/wiki/Failure_mode_and_effects_analysis "Failure mode and effects analysis").[^17] [^18] [^19]

### Requirements translation

![](https://upload.wikimedia.org/wikipedia/en/thumb/2/2f/Requirement_Translation_Example.jpg/500px-Requirement_Translation_Example.jpg)

Example requirement translation

![](https://upload.wikimedia.org/wikipedia/en/thumb/0/04/Requirements_Behavior_Tree_Integration.png/500px-Requirements_Behavior_Tree_Integration.png)

Requirements behavior tree integration

### Requirement integration

Once an integrated behavior tree has been composed, there are a number of important operations that can be performed upon it.

In general, many defects become much more visible when there is an integrated view of the requirements [^2] and each requirement has been placed in the behavior context where it needs to execute. For example, it is much easier to tell whether a set of conditions or events emanating from a node is complete and consistent. The traceability tags also make it easy to refer back to the original natural-language requirements. There is also the potential to automate a number of defect and consistency checks on an integrated behavior tree.[^20]

When all defects have been corrected and the IBT is logically consistent and complete, it becomes a model behavior tree (MBT), which serves as a [formal specification](https://en.wikipedia.org/wiki/Formal_specification "Formal specification") for the system's behavior that has been constructed out of the original requirements. This is the clearly defined stopping point for the analysis phase. With other [modeling notations](https://en.wikipedia.org/wiki/Modeling_languages "Modeling languages") and methods (i.e. [UML](https://en.wikipedia.org/wiki/Unified_Modeling_Language "Unified Modeling Language")), it is less clear-cut when modelling can stop.[^21] In some cases, parts of a model behavior tree may need to be transformed to make the specification [executable](https://en.wikipedia.org/wiki/Executable "Executable"). Once an MBT has been made executable, it is possible to carry out a number of other dependability checks.

#### Simulation

A model behavior tree can be readily simulated to explore the dynamic properties of the system. Both a symbolic tool and a graphics tool have been constructed to support these activities.[^22] [^23]

#### Model checking

A translator has been written to convert a model behavior tree into the "actions systems" language. This input can then be fed into the SAL Model checker [^24] [^25] to allow checks to be made as to whether certain safety and security properties are satisfied.[^18] [^26]

[Model checking](https://en.wikipedia.org/wiki/Model_checking "Model checking") has often been applied to system models to check that hazardous states can’t be reached during normal operation of the system.[^27] It is possible to combine model-checking with behavior trees to provide automated support for [failure mode and effects analysis](https://en.wikipedia.org/wiki/Failure_mode_and_effects_analysis "Failure mode and effects analysis") (FMEA).[^18] The advantage of using behavior trees for this purpose is that they allow the [formal method](https://en.wikipedia.org/wiki/Formal_method "Formal method") aspects of the approach to be hidden from non-expert users.

#### Requirement changes

The ideal sought when responding to a change in the [functional requirements](https://en.wikipedia.org/wiki/Functional_requirements "Functional requirements") for a system is that it can be quickly determined:

- where to make the change,
- how the change affects the architecture of the existing system,
- which components of the system are affected by the change, and,
- what behavioral changes will need to be made to the components (and their interfaces) that are affected by the change of requirements.[^28]

Because a system is likely to undergo many changes over its service life, it is necessary to record, manage, and optimize its evolution driven by these changes.

A traceability model, which uses behavior trees as a formal notation to represent functional requirements, reveals change impacts on different types of design constructs (documents) caused by the changes of the requirements.[^29] The model introduces the concept of evolutionary design documents that record the change history of the designs. From these documents, any version of a design document, as well as the difference between any two versions, can be retrieved. An important advantage of this model is that automated tools can support a major part of the procedure to generate these evolutionary design documents.[^20]

The behavior tree representation of the integrated behavior of the system offers several important advantages as an executable model. It clearly separates the tasks of *component integration* from the task of individual *component implementation*. The integrated system behavior resulting from requirement integration can serve as a foundation for design decisions. The result is a design behavior tree (DBT):[^5] an executable multi-thread component integration specification that has been built out of the original requirements.

Behavior tree models are executed in a virtual machine called the behavior run-time environment (BRE). The BRE links together [components](https://en.wikipedia.org/wiki/Component-based_software_engineering#Software_component "Component-based software engineering") using [middleware](https://en.wikipedia.org/wiki/Middleware "Middleware"),[^30] allowing components to be independent programs written in one of several languages that can be executed in a [distributed environment](https://en.wikipedia.org/wiki/Distributed_computing "Distributed computing"). The BRE also contains an expression [parser](https://en.wikipedia.org/wiki/Parser "Parser") that automatically performs simple operations to minimize the amount of code required to be manually implemented in the component.

Executable behavior trees have been developed for case studies [^21] including automated train protection,[^31] mobile robots with a dynamic object following, an ambulatory infusion pump,[^19] and traffic light management systems. A version of the BRE suited for embedded systems (eBRE) is also available, with reduced functionality tailored for small-footprint microcontrollers.

## Applications

Behavior tree modeling can and has been applied to a diverse range of applications over a number of years. Some of the main application areas are described below.

### Large-scale systems

Modeling large-scale systems with extensive sets of natural-language requirements has always been a major focus for testing behavior trees and the overall behavior engineering process. Conducting these evaluations and trials of the method has involved work with a number of industry partners and government departments in Australia. The systems studied have included a significant number of defense systems, enterprise systems, transportation systems, information systems, health systems, and sophisticated control systems with stringent safety requirements. The results of these studies have all been classified as commercial-in-confidence. However, the results of the extensive industry trials [^3] [^4] with [Raytheon](https://en.wikipedia.org/wiki/Raytheon "Raytheon") Australia are presented below in the Industry Section. This work has shown that translating requirements into integrated static and dynamic behavior-tree views revealed substantially more major defects than the company’s standard review processes detected.[^32]

### Embedded systems

Failure of a design to meet a system's requirements can result in schedule and cost overruns.[^33] If there are also critical dependability issues, not satisfying system requirements can have life-threatening consequences.[^34] However, in current approaches, ensuring that requirements are met is often delayed until late in the development process, during a cycle of testing and debugging..[^35] This work describes how the system development approach, behavior engineering, can be used to develop software for [embedded systems](https://en.wikipedia.org/wiki/Embedded_system "Embedded system").[^26]

Many large-scale systems consist of a mixture of co-dependent software and hardware. The different nature of software and hardware means they’re often modeled separately using different approaches. This can subsequently lead to integration problems due to incompatible assumptions about hardware/software interactions.[^31] These problems can be overcome by integrating behavior trees with the [Modelica](https://en.wikipedia.org/wiki/Modelica "Modelica") [mathematical modeling](https://en.wikipedia.org/wiki/Mathematical_modelling "Mathematical modelling") approach.[^31] The environment and hardware components are modeled using Modelica and integrated with an executable software model that uses behavior trees.

To ensure correct implementation of complex [access control](https://en.wikipedia.org/wiki/Access_control "Access control") requirements, it is important that the validated and verified requirements are effectively integrated with the rest of the system.[^36] It is also important that the system can be validated and verified early in the development process. An integrated, [role-based access control](https://en.wikipedia.org/wiki/Role-based_access_control "Role-based access control") model has been developed.[^37] The model is based on the graphical behavior tree notation and can be validated by [simulation](https://en.wikipedia.org/wiki/Simulation "Simulation"), as well as verified using a [model checker](https://en.wikipedia.org/wiki/Model_checker "Model checker"). Using this model, access control requirements can be integrated with the rest of the system from the outset, because: a single notation is used to express both access control and [functional requirements](https://en.wikipedia.org/wiki/Functional_requirements "Functional requirements"); a systematic and incremental approach to constructing a formal behavior tree specification can be adopted; and the specification can be simulated and model checked. The effectiveness of the model has been evaluated using a case study with distributed access control requirements.[^36]

### Biological systems

Because behavior trees describe complex behavior, they can be used for describing a range of systems not limited to those that are computer-based.[^38]

While behavior trees have become popular for modeling the [artificial intelligence](https://en.wikipedia.org/wiki/Artificial_intelligence "Artificial intelligence") in computer games such as [Halo](https://en.wikipedia.org/wiki/Halo_\(franchise\) "Halo (franchise)") [^39] and [Spore](https://en.wikipedia.org/wiki/Spore_\(2008_video_game\) "Spore (2008 video game)"),[^40] these types of trees are very different from the ones described on this page and are closer to a combination of hierarchical [finite-state machines](https://en.wikipedia.org/wiki/Finite-state_machine "Finite-state machine") or [decision trees](https://en.wikipedia.org/wiki/Decision_trees "Decision trees"). Soccer-player modeling has also been a successful application of behavior trees.[^41] [^42]

### Model-Based Testing

[Model-based testing](https://en.wikipedia.org/wiki/Model-based_testing "Model-based testing") is an approach to software testing that requires testers to create test models from requirements of Software Under Test (SUT). Traditionally, modeling languages such as UML statecharts, finite-state machines (FSMs), extended finite-state machines (EFSMs), and flowcharts have been used. Recently, an interesting approach in which Event-Driven Swim Lane [Petri Net](https://en.wikipedia.org/wiki/Petri_net "Petri net") (EDSLPN) is used as the modeling language also appeared. Behavior tree notation should be considered as a good modeling notation to MBT also, and it has a few advantages among other notations:

1. It has the same expressiveness level as UML state charts and EDSLPN.
2. It is intuitive to use as a modeling notation due to its graphical nature.
3. Each behavior tree node has a requirement tag; these greatly facilitate the creation of a [traceability matrix](https://en.wikipedia.org/wiki/Traceability_matrix "Traceability matrix") from requirement to test artifact.[^43]
![](https://upload.wikimedia.org/wikipedia/en/thumb/9/94/Behavior_Engineering_Support_Environment.png/500px-Behavior_Engineering_Support_Environment.png)

Screenshot of behavior engineering support environment tool

![](https://upload.wikimedia.org/wikipedia/en/a/a6/Integrated_Behavior_Tree_Larger_System.png)

Integrated behavior tree – larger system (more than 1000 requirements)

The first industry trials to test the feasibility of the method and refine its capability were conducted in 2002. Over the last three years, a number of systematic industry trials on large-scale defense, transportation, and enterprise systems have been conducted.[^3] [^32] This work has established that the method scales to systems with large numbers of requirements but also that it is important to use tool support [^22] [^44] in order to efficiently navigate and edit the resultant large integrated views of graphical data. On average, over a number of projects, 130 confirmed major defects per 1000 requirements have consistently been found after normal reviews and corrections have been made.[^32] With less mature requirements sets, much higher defect rates have been observed.

## Advantages

As a behavior modeling representation, behavior trees have a number of significant benefits and advantages:

- They employ a well-defined and effective strategy for dealing with requirement complexity, particularly where the initial needs of a system are expressed using hundreds or thousands of requirements written in natural language. This significantly reduces the risk on large-scale projects.[^32]
- By rigorously translating then integrating requirements at the earliest possible time, they provide a more effective means for uncovering requirement defects than competing methods.[^32] [^45]
- They employ a single, simple notation for [analysis](https://en.wikipedia.org/wiki/Analysis "Analysis"), [specification](https://en.wikipedia.org/wiki/Specification_\(computing\) "Specification (computing)"), and to represent the behavior design of a system.
- They represent the system behavior as an executable integrated whole.
- They build the behavior of a system out of its [functional requirements](https://en.wikipedia.org/wiki/Functional_requirements "Functional requirements") in a directly traceable way, which aids [verification and validation](https://en.wikipedia.org/wiki/Verification_and_validation "Verification and validation").[^22] [^37]
- They can be understood by [stakeholders](https://en.wikipedia.org/wiki/Stakeholder_\(corporate\) "Stakeholder (corporate)") without the need for [formal methods](https://en.wikipedia.org/wiki/Formal_methods "Formal methods") training. By strictly retaining the vocabulary of the original requirements, this eases the burden of understanding.
- They have a [formal semantics](https://en.wikipedia.org/wiki/Semantics_of_programming_languages "Semantics of programming languages"),[^17] they support [concurrency](https://en.wikipedia.org/wiki/Concurrency_\(computer_science\) "Concurrency (computer science)"), they are [executable](https://en.wikipedia.org/wiki/Executable "Executable"), and they can be [simulated](https://en.wikipedia.org/wiki/Simulated "Simulated"), [model checked](https://en.wikipedia.org/wiki/Model_checking "Model checking"), and used to undertake [failure mode and effects analysis](https://en.wikipedia.org/wiki/Failure_mode_and_effects_analysis "Failure mode and effects analysis").[^18]
- They can be used equally well to model human processes, to analyze contracts,[^38] to represent forensic information, to represent biological systems, and many other applications. In each case, they deliver the same benefits in terms of managing complexity and seeing things as a whole. They can also be used for [safety critical systems](https://en.wikipedia.org/wiki/Safety-critical_system "Safety-critical system"),[^19] [embedded systems](https://en.wikipedia.org/wiki/Embedded_system "Embedded system"),[^26] and [real-time systems](https://en.wikipedia.org/wiki/Real-time_systems "Real-time systems").[^46] [^47] [^48]

## See also

- [Behavioral engineering](https://en.wikipedia.org/wiki/Behavioral_engineering "Behavioral engineering")
- [Modeling language](https://en.wikipedia.org/wiki/Modeling_language "Modeling language")

## References

## External links

- [Behavior Engineering](http://www.beworld.org/BE/)
- [Raytheon Australia supports pioneering systems research](https://web.archive.org/web/20110220113558/http://www.raytheon.com.au/rtnwcm/groups/rau/documents/download/rau_factsheets_behaviortrees.pdf)
- [ARC Centre for Complex Systems – ACCS Program: Dependable Complex Computer-Based Systems](http://www.accs.uq.edu.au/projectsDCS.html)
- [Australian Research Council – Outcomes: Taming Complexity](http://arc.realviewtechnologies.com/default.aspx?iid=8075&startpage=page0000030&xml=outcomes.xml)

[^1]: Lindsay, Peter A. (1 September 2010). ["Behavior Trees: From Systems Engineering to Software Engineering"](https://doi.org/10.1109/sefm.2010.11). *2010 8th IEEE International Conference on Software Engineering and Formal Methods*. IEEE. pp. 21– 30. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1109/sefm.2010.11](https://doi.org/10.1109%2Fsefm.2010.11). [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1-4244-8289-4](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4244-8289-4 "Special:BookSources/978-1-4244-8289-4").

[^2]: Dromey, R.G. 2007. [Principles for Engineering Large-Scale Software-Intensive Systems](http://www.beworld.org/BE/resource/presentation/Eng-LargeScale-Systems.pdf)

[^3]: Boston, J. 2008. [Raytheon Australia supports pioneering systems research](http://www.raytheon.com.au/Default.aspx?x=501) [Archived](https://web.archive.org/web/20090915050723/http://www.raytheon.com.au/Default.aspx?x=501) 15 September 2009 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine")

[^4]: Raytheon Australia, 2008. [Understanding grows on Behavior Trees](http://www.raytheon.com.au/Files/Behavior%20Trees.pdf) [Archived](https://web.archive.org/web/20090915050633/http://www.raytheon.com.au/Files/Behavior%20Trees.pdf) 15 September 2009 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine")

[^5]: R.G.Dromey, [From Requirements to Design: Formalizing the Key Steps](http://www.behaviorengineering.org/publications/dromey/K1-Dromey.pdf) [Archived](https://web.archive.org/web/20110725054005/http://www.behaviorengineering.org/publications/dromey/K1-Dromey.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), (Invited Keynote Address), SEFM-2003, IEEE International Conference on Software Engineering and Formal Methods, Brisbane, Sept. 2003, pp. 2–11.

[^6]: Behavior Engineering. [Composition Trees](http://www.behaviorengineering.org/index.php?option=com_content&task=view&id=24&Itemid=34) [Archived](https://web.archive.org/web/20090302063932/http://www.behaviorengineering.org/index.php?option=com_content&task=view&id=24&Itemid=34) 2 March 2009 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine")

[^7]: Winter, K. 2007. [Formalising Behaviour Trees with CSP](http://espace.library.uq.edu.au/eserv/UQ:100586/Formalising_behaviour_trees_with_csp.pdf)

[^8]: R.G.Dromey, ["Formalizing the Transition from Requirements to Design"](http://www.behaviorengineering.org/publications/dromey/Dromey-Chapter-Final-20051.pdf) [Archived](https://web.archive.org/web/20110725053952/http://www.behaviorengineering.org/publications/dromey/Dromey-Chapter-Final-20051.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), in "Mathematical Frameworks for Component Software – Models for Analysis and Synthesis", Jifeng He, and Zhiming Liu (Eds.), World Scientific Series on Component-Based Development, pp. 156–187, (Invited Chapter) (2006)

[^9]: R.L.Glass, ["Is This a Revolutionary Idea or Not"](http://www.behaviorengineering.org/publications/Bob-Glass-GSE-CACM.pdf) [Archived](https://web.archive.org/web/20110725054100/http://www.behaviorengineering.org/publications/Bob-Glass-GSE-CACM.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), Communications of the ACM, Vol. 47(11), pp. 23–25, Nov. 2004.

[^10]: R.G.Dromey, ["Climbing Over the ‘No Silver Bullet’ Brick Wall"](http://www.behaviorengineering.org/publications/dromey/Dromey.pdf) [Archived](https://web.archive.org/web/20110725054117/http://www.behaviorengineering.org/publications/dromey/Dromey.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), IEEE Software, Vol. 23, No. 2, pp. 118–120, (March 2006)

[^11]: R.G.Dromey, Genetic Software Engineering – Simplifying Design Using Requirements Integration, IEEE Working Conference on Complex and Dynamic Systems Architecture, Brisbane, Dec 2001.

[^12]: A. Woolfson, Life Without Genes, Flamingo, 2000, [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-00-255618-9](https://en.wikipedia.org/wiki/Special:BookSources/0-00-255618-9 "Special:BookSources/0-00-255618-9")

[^13]: Berlin, I. The Crooked Timber of Humanity: Chapters in the History of Ideas, Ed., H.Hardy, Princeton University Press, 1998 [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-691-05838-5](https://en.wikipedia.org/wiki/Special:BookSources/0-691-05838-5 "Special:BookSources/0-691-05838-5")

[^14]: ["Behavior Engineering World » History of Behavior Engineering"](https://www.beworld.org/BE/home/history-of-behavior-engineering/). Retrieved 24 May 2025.

[^15]: Colvin, R., Grunske, L., Winter, K. 2007 [Probabilistic Timed Behavior Trees](http://www.behaviorengineering.org/publications/grunske/IFM1.pdf) [Archived](https://web.archive.org/web/20110725054158/http://www.behaviorengineering.org/publications/grunske/IFM1.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine")

[^16]: Dromey, R.G. ["Genetic Design: Amplifying Our Ability to Deal With Requirements Complexity"](http://www.behaviorengineering.org/publications/dromey/Dromey-LNCS-Final2-new.pdf) [Archived](https://web.archive.org/web/20110725054508/http://www.behaviorengineering.org/publications/dromey/Dromey-LNCS-Final2-new.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), in S.Leue, and T.J. Systra, Scenarios, Lecture Notes in Computer Science, LNCS 3466, pp. 95–108, 2005.

[^17]: Colvin, R., Hayes, I.J. 2006 [A Semantics for Behavior Trees](http://www.accs.uq.edu.au/documents/TechnicalReports/ACCS_TR_07_01.pdf)

[^18]: L.Grunske, P.Lindsay, N.Yatapanage, K.Winter, [An Automated Failure Mode and Effect Analysis Based on High-Level Design Specification with Behavior Trees](https://doi.org/10.1007%2F11589976_9), Fifth International Conference on Integrated Formal Methods (IFM-2005), Eindoven, The Netherlands, 2005.

[^19]: Zafar, S. and Dromey, R. G., (2005), [Integrating Safety and Security Requirements into Design of an Embedded System.](http://www.behaviorengineering.org/publications/dromey/Zafar-IntegratingRequirments.pdf)[Archived](https://web.archive.org/web/20110725054345/http://www.behaviorengineering.org/publications/dromey/Zafar-IntegratingRequirments.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine") Asia-Pacific Software Engineering Conference 2005, 15–17 December, Taipei, Taiwan. IEEE Computer Society Press. pp. 629–636.

[^20]: Smith, C., Winter, K., Hayes, I., Dromey, R.G., Lindsay, P., Carrington, D.: [An Environment for Building a System Out of Its Requirements](https://ieeexplore.ieee.org/document/1342775), 19th IEEE International Conference on Automated Software Engineering, Linz, Austria, Sept. (2004).

[^21]: Dromey, R.G. [Using Behavior Trees to Model the Autonomous Shuttle System](http://www.behaviorengineering.org/publications/dromey/Dromey-SCESM-2004N.pdf) [Archived](https://web.archive.org/web/20110725054354/http://www.behaviorengineering.org/publications/dromey/Dromey-SCESM-2004N.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), 3rd International Workshop on Scenarios and State Machines: Models, Algorithms, and Tools (SCESM04) ICSE Workshop W5S, Edinburgh, 25 May 2004

[^22]: L.Wen, R.Colvin, K.Lin, J.Seagrott, N.Yatapanage, R.G.Dromey, 2007, ["Integrare, a Collaborative Environment for Behavior-Oriented Design"](http://www98.griffith.edu.au/dspace/bitstream/10072/18625/1/43991_1.pdf), in Proceedings of the Fourth International Conference on Cooperative Design, Visualization and Engineering, LNCS 4674, pp. 122–131, 2007

[^23]: C. Sun, S. Xia, D. Sun, D. Chen. H.F. Shen, W. Cai: ["Transparent adaptation of single-user applications for multi-user real-time collaboration"](http://portal.acm.org/citation.cfm?doid=1188816.1188821), ACM Transactions on Computer-Human Interaction, Vol. 13, No.4, December 2006, pp. 531–582.

[^24]: Bensalem, S., Ganesh, V., Lakhnech, Y., Muñoz, C., Owre, et al.: "An Overview of SAL", Fifth NASA Langley Formal Methods Workshop (LFM 2000), 2000, pp. 187–196.

[^25]: Rushby, J. [Automated Formal Methods 2006](http://fm.csl.sri.com/AFM06/slides/Rushby-intro-tutorial.pdf) AFM-2006, Automated Formal Methods 2006, Seattle, August 2006, pp. 6–7.

[^26]: Zafar, S. and Dromey, R. G., 2005. [Managing Complexity in Modelling Embedded Systems.](http://www.behaviorengineering.org/publications/dromey/Zafar-SETE2005-ManagingComplexity.pdf)[Archived](https://web.archive.org/web/20110725054400/http://www.behaviorengineering.org/publications/dromey/Zafar-SETE2005-ManagingComplexity.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine") Systems Engineering/Test and Evaluation Conference 2005, 7–9 November, Brisbane, Australia

[^27]: Grunske, L., Colvin, R., Winter, K. Probabilistic Model-Checking Support for FMEA Quantitative Evaluation of Systems. QEST 2007. Fourth International Conference on the Quantitative Evaluation of Systems, 17-19 Sept. 2007 pp. 119–128

[^28]: Wen, L., Dromey, R.G. 2007. [From Requirements Change to Design Change: A Formal Path](http://www.behaviorengineering.org/images/publications/wen_l_dromey_r_g_gse_change.pdf)

[^29]: Wen, L., Dromey, R.G. 2005. [Architecture Normalization for Component-Based Systems](http://www.behaviorengineering.org/publications/wen/journal.pdf) [Archived](https://web.archive.org/web/20110725054411/http://www.behaviorengineering.org/publications/wen/journal.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine") Proceedings of the 2nd International Workshop on Formal Aspects of Component Software FACS'05, pp. 247–261.

[^30]: RTI Inc. 2007 "Meeting Real-Time Requirements in Integrated Defense Systems", [RTI White Paper](http://www.rti.com/mk/defense_systems.html) [Archived](https://web.archive.org/web/20080920033015/http://www.rti.com/mk/defense_systems.html) 20 September 2008 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine").

[^31]: Myers, T., Fritzson, P., Dromey, R.G. 2008. [Seamlessly Integrating Software & Hardware Modelling for Large-Scale Systems.](http://www.ida.liu.se/~petfr/paperlinks/2008-07-Myers-Fritzson-Dromey-EOOLT2008-HardwareSoftwareModeling.pdf) 2nd International Workshop on Equation-Based Object-Oriented Languages and Tools (EOOLT 2008), Cyprus, July 2008. pp. 5–15.

[^32]: Powell, D. 2007. [Requirements Evaluation Using Behavior Trees – Findings from Industry](http://www.behaviorengineering.org/docs/ASWEC07_Industry_Powell.pdf) [Archived](https://web.archive.org/web/20110725061927/http://www.behaviorengineering.org/docs/ASWEC07_Industry_Powell.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine")

[^33]: Barker, D. 2000. [Requirements modeling technology: a vision for better, faster, and cheaper systems.](https://ieeexplore.ieee.org/document/890177) Proceedings from VHDL International Users Forum Fall Workshop, 2000. pp. 3–6.

[^34]: Leveson, N. G. Safeware: System Safety and Computers: \[a guide to preventing accidents and losses caused by technology\]. Addison-Wesley Publishing Company, 1995. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-201-11972-2](https://en.wikipedia.org/wiki/Special:BookSources/0-201-11972-2 "Special:BookSources/0-201-11972-2")

[^35]: Futrell, R. T., Shafer, D.F., Shafer, L.I. Quality Software Project Management (Software Quality Institute Series). Prentice Hall, 2002 [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-13-091297-2](https://en.wikipedia.org/wiki/Special:BookSources/0-13-091297-2 "Special:BookSources/0-13-091297-2")

[^36]: Zafar, S. Colvin, R., Winter, K., Yatapanage, N., Dromey, R.G. [Early Validation and Verification of a Distributed Role-Based Access Control Model.](https://ieeexplore.ieee.org/document/4425884) 14th Asia-Pacific Software Engineering Conference, Nagoya, Japan, December 2008. pp. 430–437.

[^37]: Zafar, S., K.Winter, R.Colvin, R.G.Dromey, ["Verification of an Integrated Role-Based Access Control Model"](http://www.behaviorengineering.org/publications/dromey/Zafar_Integrated_BTRBAC.pdf) [Archived](https://web.archive.org/web/20110725061854/http://www.behaviorengineering.org/publications/dromey/Zafar_Integrated_BTRBAC.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), 1st International Workshop – Asian Working Conference on Verified Software (AWCVS'06), pp 230-240, Macao, Oct. 2006.

[^38]: Milosevic, Z., Dromey, R.G. [On Expressing and Monitoring Behavior in Contracts](https://ieeexplore.ieee.org/document/1137692), EDOC 2002, Proceedings, 6th International Enterprise Distributed Object Computing Conference, Lausanne, Switzerland, Sept. 2002, pp. 3-14.

[^39]: Damian Isla [Handling Complexity in the Halo 2 AI.](https://www.gamedeveloper.com/programming/gdc-2005-proceeding-handling-complexity-in-the-i-halo-2-i-ai)

[^40]: Chris Hecker [My Liner Notes for Spore](http://chrishecker.com/My_Liner_Notes_for_Spore/Spore_Behavior_Tree_Docs)

[^41]: Xiao-Wen Terry Liu and Jacky Baltes [An Intuitive and Flexible Architecture for Intelligent Mobile Robots](http://www.cs.umanitoba.ca/~jacky/Publications/pdf/liu04:_intuit_flexib_archit_intel_mobil_robot.pdf) 2nd International Conference on Autonomous Robots and Agents, December 13–15, 2004 Palmerston North, New Zealand

[^42]: Yukiko Hoshino, Tsuyoshi Takagi, Ugo Di Profio, and Masahiro Fujita [Behavior description and control using behavior module for personal robot](http://web.mit.edu/zoz/Public/ICRA04-Hoshino.pdf)

[^43]: . *testerhome.com*. Retrieved 12 June 2025.

[^44]: Phillips, V., (Raytheon Australia), ["Implementing a Behavior Tree Analysis Tool Using Eclipse Development Frameworks"](http://www.behaviorengineering.org/images/publications/dromey2/bese_master_v2.ppt), Australian Software Engineering Conference (ASWEC’08), Perth, March 2008

[^45]: Boston, J., (Raytheon Australia), [Behavior Trees – How they improve Engineering Behaviour?](http://www.behaviorengineering.org/images/publications/dromey2/sp8_powerpoint_jim_boston.pdf), 6th Annual Software and Systems Engineering Process Group Conference (SEPG 2008), Melbourne, Aug. 2008.

[^46]: Lin, K., Chen, D., Sun, C., Dromey, R.G., [A Constraint Maintenance Strategy and Applications in real-time Collaborative Environments](http://www.behaviorengineering.org/publications/kailin/CDVEO5_Kevin.pdf), 2nd International Conference on Cooperative Design, Visualization and Engineering (CDVE2005), 2005.

[^47]: Lin, K., Chen, D., Dromey, R.G., Sun, CZ.: [Multi-way Dataflow Constraint Propagation in Real-time Collaborative Systems](http://www.behaviorengineering.org/publications/kailin/IEEE06_Kevin.pdf) [Archived](https://web.archive.org/web/20110725061427/http://www.behaviorengineering.org/publications/kailin/IEEE06_Kevin.pdf) 25 July 2011 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), IEEE, The 2nd International Conference on Collaborative Computing: Networking, Applications and Worksharing (CollaborateCom 2006), Atlanta, Georgia, USA, Nov, 2006.

[^48]: Grunske, L., Winter, K., Colvin, R., ["Timed Behavior Trees and their application to verifying real-time systems"](http://www.behaviorengineering.org/publications/grunske/ASWEC20072.pdf) [Archived](https://web.archive.org/web/20081118165542/http://www.behaviorengineering.org/publications/grunske/ASWEC20072.pdf) 18 November 2008 at the [Wayback Machine](https://en.wikipedia.org/wiki/Wayback_Machine "Wayback Machine"), Proceedings of 18th Australian Conference on Software Engineering (AEWEC 2007), April 2007, accepted for publication.