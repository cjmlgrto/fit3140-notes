[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Design Quality

- A "good design" is one that results in high quality software
- "High quality software" refers to software that rates high in terms of:
	- Functionality
	- Reliability
	- Usability
	- Efficiency
	- Maintainability
	- Portability
- Quality can be measured as a result of "external" characteristics (i.e. the final product) or at the lower-level (i.e. code)
- In the eXtreme Programming view: _design can and should evolve over time_ (and _simple_ is better)

## Software Simplicity

- _Appropriate for intended audience_: the people using the design can understand it
- _Communicative_: elements of the system can be communicated to future users
- _Factored_: "data, structure or logic should appear to exist in one place in the system"
- _Minimal_: "Within the above three constraints, the system should have the fewest elements possible"

## Coupling and Cohesion

- **Coupling** is the degree to which each program module relies on each one of the other modules
- **Cohesion** is a measure of how strongly-related or focused the responsibilities of a single module are (i.e. if the methods in a given class tend to be similar in many aspects, then the class is said to have _high cohesion_)

The goal is to **minimise coupling** and **maximise cohesion**.

- The **Single Responsibility Principle** states that "there should never be more than one reason for a class to change"
- The **Liskov Substitution Principle** states that "functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it"
- The **Open-Closed Principle** states that "software entities (i.e. classes, modules, functions, etc.) should be open for extension, but closed for modification
	- This can be achieved by having a concrete base class, and re-using code by inheritance
- The **Interface Segregation Principle (ISP)** states that "clients should not be forced to depend upon interfaces they do not use"
- The **Dependency Inversion Principle** states that "high-level modules should not depend on low-level modules. Both should depend on abstractions" (i.e. abstractions should not depend on details; details should depend on abstractions)

### The Circle-Ellipse Problem

- Suppose you have a class `Ellipse` with the method, `Stretch`
- Now suppose it has a sub-class called `Circle`
- By the _Liskov Substitution Principle_, `Circle` must also inherit the method, `Stretch`
- But when a `Circle` is stretched, it is no-longer a circle!

