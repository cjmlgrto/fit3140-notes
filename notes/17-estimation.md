[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Estimation

- A "back-of-the-envelope" estimation is often required to quickly and pre-emptively calculate tradeoffs in design and implementation
- They are rough calculations, typically scribbled onto the back of any available writing surface (such as the back of an actual envelope)
- It is more than a guess, but less accurate than a real calculation or mathematical proof
- Estimation is used to weigh and survey potential options (more thinking than simply common sense or intuition)
- The outcomes of estimation are always the following:
	- "OK"
	- "not OK"
	- "Don't know"

But estimation is no silver bullet:

> It's almost impossible to identify performance bottlenecks before the programs is completely working. Programmers almost _never_ target the right area ahead of time.

— McConnell, 1993

- However, data structures, external interfaces, network protocols are great examples of where to estimate implementation/cost/benefits/performance etc.
- If estimation wasn't done, optimising the examples above would cost too much
- Contention: bad design decisions lead to the worst performance bottlenecks


#### Orders of Magnitude

- Big-O complexity is almost often never documented in APIs
- It is important to consider what the biggest dataset may be applied
- Or even, how often it will be applied