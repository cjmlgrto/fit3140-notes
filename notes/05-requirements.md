[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Requirements Gathering

- **Requirements** — the _what_
- **Design** — the _how_
- Often, the above two get confused because they exist in a continuum
- In the Waterfall Model (and most other software lifecycle models)

## Traditional Requirements Gathering

### Software Requirements Specification

- A detailed document that describes the requirements for the entire system
- Agreed upon by customer and developers
- Long (e.g. can be 40-pages long for a one-semester software team project)
- Is a combination of normal English text, UML use-case diagrams, and "requirementese"

### Some Problems

- Detailed documentation can be difficult to produce
- Non-programmers (sometimes even some programmers) can be poor at describing things in sufficient detail to construct use cases
- Client's professed wants and actual needs are usually different
- Are their wants/needs actually feasible given cost/budget constraints?
- Customers are better at telling what they don't want than what they do want

### Consequences

- Knowing everything in advance is infeasible
- But if everything is not known in advance, the project can fail
- Hence: processes are needed that can cope with change/uncertainty in requirements
- At a minimum, this suggest prototyping and incremental development
- Agile principles: embrace (and expect) change

## Agile Approach to Requirements

- Involves gathering detailed requirements as projects advance
- Captures requirements in the form of **User Stories** (chunks of functionality that can be implemented, tested, and ready for demo in _one iteration_)
- Best communicated directly between developers and customer/user
- However, need some preliminary understanding of the problem domain/project vision as a guide for all User Stories

### The On-Site Customer

- Rather than super-detailed requirements documents, have the customer present at all times during development
- As developers implement, they can ask the customer then and there about details
- At worst, the "customer" contacts the relevant stakeholder and asks them
- Fewer documents, closer to what's actually required, and instant feedback
- However, _requires a switched-on, committed customer!_

### Documentation

- The most efficient and effective way of conveying information to and within a development team is face-to-face conversation
- Contention: this is often, but not always the best case — since people's memories are fallible, and writing need not be repeated — thus the need for documentation
- However: writing documetation costs time and therefore money
- Big doucments are very expensive to produce
- If expected benefit from writing document exceeds costs, write the document to the level of detail required _and no more_
- Therefore, the most concise and valuable requirement documentation will at least include:
	- A short "vision statement"
	- Organisational context (through context diagrams and use-case diagrams, i.e. the software's position around its users)
	- Highest user priorities (as user stories)
	- Domain vocabulary (an evolving glossary of shared and agreed-upon terms)
	- Broad architecture of solution (include platform issues and very high-level design sketches)
	- Identify biggest unknowns (risks)

## User Stories

- Are small cards that:
	- describe a particular user requirement
	- provide an estimate of the effort required (e.g. in hours)
- Are designed around units of work and can be split up into more detailed "tasks" by developers later
- Do not capture every detail
- Are _testable_
- Weekly cycle — _customer_ picks which user stories to implement

### Backlog (from Scrum)

- The **Backlog** is a prioritised list of user stories
- Each story is worded in a way such that it follows the pattern: "As a ____, I want to _____"
- Can include "Tech Stories" (i.e. a chunk of tasks that needs to be done during development)
- Can also include references to external documentation and screen mockups (a picture is worth a thousand words, so mockups can be used to efficiently show what a story is describing)

### Collecting User Stories

- Done in planning between customers and developers
- Done face-to-face
- Done in planning sessions:
	- **Beck** — two types: weekly (one iteration, pick next stories) and quarterly (theme, write most user stories given a theme)
	- **Scrum** — go on backlog as needed, finishing tasks based on priority (where each task's priority is discussed with the customer during the sprint planning sessions)
	- **Cohn**: — "story-writing workshops"
- Written down on cards (or Trello, etc.)

#### Story Writing Workshops

- Gatherings of users, developers, project managers — and all other potential stakeholders
- Write as many stories as possible
- Some stories may be way too large or infeasible at this point

#### INVEST (a handy acronym)

The best user stories have the following properties:

- Independent (can be implemented without depending on other stories)
- Negotiable (flexible in its definition)
- Valuable (has value to the customer)
- Estimable
- Small
- Testable

### What about Non-Functional Requirements?

- These can be things that related to the external domain, and other technical issues such as performance, reliability, security, maintainability and usability
- These can be modeled by considering _constraints_ on user stories
	- e.g. Given the user story "As a customer, I want to be able to browse all my music", the contraint could be "Listing all the music shouldn't take longer than 0.5s"



