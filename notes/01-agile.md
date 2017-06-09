[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Intro to Agile Development

- Software Development is a formalised process of gathering client (or customer) requirements, implementation, testing and delivery.
- This is done by following a _Software Process_ — a model that describes the steps by which software is developmed, deployed and maintained.
- Some examples of Software Processes — or _Software Lifecycle Models_ — include the "Code and Fix Model", the "Waterfall Model", the "V-Model" and "Agile".

## The Waterfall Model

### Steps

1. System Requirements
2. Software Requirements
3. Analysis
4. Program Design
5. Coding
6. Testing
7. Operations

Although straight-forward, the Waterfall Model has its drawbacks, mainly because it assumes the following:

- 😓 Requirements are knowable in advanced and captured 100% correctly and communicated to designers
- 😓 Designers produce a feasible design that satisfies all requirements
- 😓 Design is feasible to code
- 😓 Coders and testers understand the design perfectly
- 😰 _And that requirements do not change during the entire development process_.

Because of the above assumed pre-conditions, the Waterfall Model _will not work in many situations_.

## The V-Model

### Steps

1. Project Definition
	- Concept of Operations
	- Requirements and Architecture
	- Detailed Design
2. Implementation
	- Coding
3. Project Test and Integration
	- Integration, Test and Verification
	- System Verification and Validation
	- Operation and Maintenance
4. Overall Verification and Validation
	- Repeat back to step 1 should any requirements change

The V-Model is a more iterative approach to the Waterfall Model, which involves repeating the requirements gathering, analysis and design phases should any requirements change.

## The Agile Model

### The Agile Manifesto

1. Individuals and Interactions > Processes and Tools
2. Software that Works > Comprehensive Documentation
3. Customer Collaboration > Contract Negotiation
4. Responding to Change > Following a Plan

### Key Features

- ✅ Risks and risk mitigation front-and-center
- ✅ Short (generally time-boxed) iterative approach
- ✅ Continuous customer involvement
- ✅ Detailed plans only for short term
- ✅ Testing integrated into development
- ✅ Requirements/design/coding are a continuum
- ✅ Small self-organising teams working in close proximity
- ✅ Concentration on a few key best practices

However, note that Agile **does not mean**:

- ❌ ...no documentation
- ❌ ...code first, think second
- ❌ ...no architecture and design
- ❌ ...no measurement
- ❌ ...software projects will always succeed
- ❌ ...any idiot can write software
- ❌ ...changes of mind will be cost-free
- ❌ ...ignores all best practices

### Pre-requisites

- Skilled People
- Customer Acceptance
- Customer Involvement

### Challenges

- Big Projects
	- If there are 1k programmers, they can't all work in proximity
	- "Flat" self-organised teams can't be built with 1k programmers
- Safety-critical Systems
	- Would you trust Aircraft Control software that's not been externally reviewed?
	- How can you review without formal documentation?
- If Agile methods fail, they will fail more quickly than the Waterfall Model