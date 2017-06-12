[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Refactoring

Sometimes, our design and implementation may not be so good:

- Maybe because we inherited some legacy code that's
	- Badly structured
	- Not well-commented
	- We don't understand it well
- Maybe because we wrote it ourselves
	- Didn't design it well (or at all) in the first place
	- Made some assumptions that didn't pan out
	- "bit rot" has set in over multiple iterations

**Refactoring** is changing the design of a software artefact _without changing what it does_.

- Most refactorings should be invisible to the code that's not involved in the refactor
- Can also be termed "cleaning up the code" to make it
	- More comprehensible
	- More extensible
	- More maintainable

### When Should we Refactor?

- When we know we're going to need to change code in the future
- When the existing design makes it hard to add new features

## Code Smells

- Features of code that may indicate a design problem
- Not actual bugs, just warning signs
- Eveng clean and well-designed code tends to become "smelly" after a while (at which point you need to change it)

### Really Long Methods

- Are hard to maintain
- Probably trying to do more than one thing
- Probably overtly complex
- Probably hard to change in order to add new functionality
- Probably hard to test

### Really Large Classes

- Too many responsibilities
- Too much going on
- Lots of responsibilities means likely to need to change with added functionality
- Lots going on means difficult to change

### Duplicate Code

- DRY: Don't Repeat Yourself

### Lots of Comments

- When there is more explanation than necessary for others to understand how it works

### Switching on Object Type

- Case statement that does a switch on some kind of indicator of the type of an object
- Makes it awkward to add new types
- Usually means you should be using polymorhpism instead

## How to Refactor

- Slowly, with small changes
- Test between changes to ensure client code still works
- Don't try to refactor as you add new code
	- Goal of development is to _add features_
	- Goal of refactoring is to fix design but _leave functionality the same_
	- Refactoring shouldn't change the results of any unit tests you have on your code

## Some Common Refactorings

### Move Method

#### Do this when:

- A method is being used more by methods of another class than by its own class (i.e. causing coupling)

#### Procedure:

- Check to see whehter other methods on the original class should also be moved
- Check subclasses and superclasses — don't move the method if it's polymorphic or things will break
- Declare the method in the new class (change the name if it makes sense to do so) and copy the code across
- Get the code working & test thoroughly
- Replace the body of the original method with a call to the new method and test again

### Move Attribute

#### Do this when:

- A class has an attribute that's used more by methods of another class than its own

#### Procedure:

- If the attribute is public, make it private and add accessors
- Declare attribute (and appropriate accessors) in target class
- Remove attribute from original class, and replace references to it with calls to accessors in new class
- Test!

### Extract Method

#### Do this when:

- You have a block of code that's repeated in multiple places
- Or you have a method that's too long and you want to break it into submethods

#### Procedure:

- Pull the block of code out into its own method
- Give it a descriptive name
- Any local variables the code block needs from its original context become parameters
- Replace the block with a call to the new method


### Extract Class

#### Do this when:

- You have a large class that you want to split into two separate classes

#### Procedure

- Decide which methods and attributes go where
- Create a new class with appropriate name (and rename the old class if its original name no longer fits)
- Give the old class an instance of the new class (as a private attribute)
- Move attributes from old class to new class, testing after each move
- Move methods from cold class to new class, testing after each move

