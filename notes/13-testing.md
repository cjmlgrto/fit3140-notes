[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Testing

**Testing** code is important, but it can't prove the non-existence of all faults. Some problems in testing include: selecting test data, conducting tests, and checking correctness of behaviour.

Types of testing:

- Functional
	- Debug
	- Regression
	- Unit
	- Integration
	- Acceptance
- Performance
- Usability

## Functional/Debug Testing

- The "debugger's intuition"
	- Limited resources available for testing
	- Want to improve reliability as much as possible
	- More faults exposed → more faults fixed
	- More faults fixed → bigger improvement in reliability
- Therefore, try to reveal as many faults as possible!
- An altnerative approach: try to make tests resemble real use

## Unit Testing

- Testing an individual module/class
- Generally has to be "debug" approach
- Often requires substantial amounts of glue code
	- Pyunit and other testing tools provide some infrastructure

## Integration/Acceptance Testing

- Testing larger "chunks" of the code
- Traditional methods encourage piecewise integration → multiple layers of integration testing
- Continuous integration, so hopefully not needed
- Acceptance tests are the "whole" system as a customer would see it
	- Traditionally agreed with customer as successful contract completion

## Regression Testing

- Testing to see whether new errors have emereged in old code, or old errors re-emerged
- Typical forms:
	- Re-running some/all existing test cases after changes
	- Running test cases designed to expose old bugs

## Performance/Stress/Load Testing

- Testing of non-functional characterstics, like performance
- Most commonly automated type of testing
- Requires a model of load, usually

## Usability Testing

- "Real users" test UI
- Inherently manual
- Expensive to do formally

## Test Case Document Template

#### Identifier

#### Setup

#### Procedure

#### Expected Output

## Specification-Based Testing

- AKA "Black-box" testing
- Testing based on the documentation, not the code
- (Grey-box testing is a combination of the two)

## Equivalence Testing

- One of a family of similar techniques
- Look at input domain to method
- Group "similar" inputs into equivalence classes
- Conduct one test from each equivalence class

## Boundary Testing

- Very often, failures occur at boundaries
- So test on boundaries
- For one single integer, two tests will usually do

## Limitations

- Testing requires us to have a specification
- In agile methods, specification is in our heads
- It's incomplete and we make it up as we go along
- So how do we do testing in these cases?