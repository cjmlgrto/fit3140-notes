[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Debugging

- **Debugging** is hard
- The further away from the initial programming task you get, the harder it gets
- That's why we spend so much effort into avoiding bugs via design and testing
- That's why we should use languages that avoid many bugs
- But debugging is unavoidable

## Debuggers

- Console debugers showed contents of registers and main memory
- Console allows step-through of programs, modification of register values, etc.
- Great as far as they go
- But they have their limits:
	- Stopping every time you want to inspect data
	- Performance issues
	- Doesn't work well on threaded/parallel debugging

## Logging

- Print messages at key points when code is executed
- Often works in situations where debuggers are too clumsy

## Debugging: A Step-By-Step Guide

### Step 1: Reproduce the Bug

- Find a test that reliable causes the bug to happen
- Unless you have this, debugging is very difficult
- "Heisenbugs" (i.e. bug works sometimes but not) and "Mandelbugs" (i.e. bug is caused by another bug, which is caused by another bug, which is caused by...) can occasionally make this a nightmare

### Step 2: Trace Symptoms

- If it's a crash, where does the crash happen?
- If it's unexpected, where does the behaviour start deviating from expected?
- Cause and effect may be quite separated, so tracing all the way back can be a lengthy process
- What's changed lately? Usually, the most-recently changed code is the obvious place to start looking.
- If you have a good repo, you can try different versions of the code until you find the exact one where the bug manifests

### Step 3: Check Faulty Assumptions

- Most of the time, bugs are the result of faulty assumptions
- So test your assumptions!
- Another way to do this is to form a hypothesis about the cause of the bug, then devise experiments to test the hypothesis
- Another fault is **Confirmation Bias**:
	- The tendency to do experiments that confirm what we already think we know
	- Instead, design experiments to falsify what you know
	- Another way to avoid this is to _explain your problem_

### Step 4: Induction

- Simply put, the process of generalising specific observations

### Step 5: Next Steps

- If you're really stuck, take a break
- Or ask for help (read the documentation, etc.)
- Or if you've found the bug:
	- Have you really understood the bug?
	- What were the incorrect assumptions?
	- Are these assumptions made elsewhere?
- If the bug was found by a customer:
	- Why wasn't the bug found in testing?
	- Why was it so hard to find once reported?
	- Have you added a regression test?

