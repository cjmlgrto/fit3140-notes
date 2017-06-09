[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Design

- In Software Development, **Design** is the process of turing a requirements specification into design documents
- **Design Documents** describe how a software product should work — and there are two types of design documents: _architectural design_ (high-level) and _detailed design_ (low-level)

## Design as Modelling

- A _design document_ is really a collection of models of different parts of a system
- Models are abstractions/simplified views of some aspect of some part of the system
- Models can help us:
	- Understand
		- Large systems can be difficult to comprehend
		- Different models allow us to "view the forest, trees and their individual leaves" when necessary
	- Communication
		- Capture and document decisions
		- Represent and explain concepts visually
- Models offer a template that can be used when constructing the system
- Models are great for when you need to explain or talk about the design to someone who's not in the design team

### How to Create Models

- Start with the model who is aimed at
- Keep in mind:
	- Model to understand
	- Model to communicate
	- Keep the model simple
- Model in teams as it reduces risk
- Use simple tools (i.e. whiteboards, paper & pencil, etc.)

### Classes of Models

One model is not enough: we need to be able to comprehend a complex system in its entirety. As such, the following classes of models exist:

- **Static Models** — involves capturing the structure of the system
- **Dynamic Models** — captures the interaction between components, and captures changes of state within components over time

### Levels of Models

- Models can be made to model the "whole" system or some small part of it
- Models can also be made to model "business processes" or low-level interaction between classes, event within a class if necessary

### Formal Models

- Some modeling notations have formal, strictly-defined rules
- Automated ways to _prove_ things about the model
- Provides a structured vocabulary so models are easy to understand

### Unified Modelling Language

There are 14 types of UML diagrams:

- **Structure Diagram** (Static Modelling)
	- [Class Diagram](http://www.agilemodeling.com/artifacts/classDiagram.htm)
	- Component Diagram
	- Object Diagram
	- Profile Diagram
	- Composite Structure Diagram
	- Deployment Diagram
	- Package Diagram
- **Behaviour Diagram** (Dynamic Modelling)
	- [Activity Diagram](http://www.agilemodeling.com/artifacts/activityDiagram.htm)
	- Use-Case Diagram
	- [State Machine Diagram](http://www.agilemodeling.com/artifacts/stateMachineDiagram.htm)
	- Interaction Diagram
		- [Sequence Diagram](http://www.agilemodeling.com/artifacts/sequenceDiagram.htm)
		- Communication Diagram
		- Interaction Overview Diagram
		- Timing Diagram
  