[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Tradeoffs
Programmers are expected to write fast and efficient software at a low cost— but in the real world, this never usually occurs.

## Performance versus Cost
* In software engineering, **performance** is "where the system meets performance goals specified by the customer"
* In the context of interaction with the world it is "where the system waits for the world, not the other way around"
* Where that interaction is with a human (in which "perceived waiting for the system is minimised") — i.e. it's an illusion

### Average-Case, Worst-Case and the n-th % Case

* In many safety-critical systems, worst-case performance is key — e.g. "The ESC will detect a skid condition within 30ms" (may even have to prove this)
* Others, average-case can be important — i.e. where algorithmic complexity is a factor based on average input
* Still others, n-th % case can also matter — e.g. 99% of all GET requests need to work

### Cost

Can include (but not limited to):

* Time and space constraints
* Hardware (CPU / GPU / RAM /Storage infrastructure)
* Network (Infrastructure / Service)
* Energy (Battery Life / Operating)
* Development ("Hardware is cheap but programmers are expensive")
* Fast code may be harder to write, harder to debug, more bugs deployed, less maintainable or even less portable

One of the best ways to facilitate decision-making in terms of weighing in cost versus performance is by graphing it and comparing where each option stands compared to the others.

### Performance

Technology advances, and it does improve performance. Some technologies have been developed solely to increase software efficiency, such as parallel computation, distributed computation, solid-state mass storage, and further increases in CPU and networking speeds.

#### Latency versus Bandwidth (freeway analogy)
* **Latency** — travel time along a freeway
* **Bandwidth** — width of a freeway
* Low latency plus high bandwidth means faster data
* As a rule of thumb: design for latency, buy bandwidth

#### Amdahl's Law
* Let S = number of distributed processors
* Let P = original program runtime
* Then the maximum speed up time <= 1/([1-P]+[P/S])



# Tradeoffs
Programmers are expected to write fast and efficient software at a low cost— but in the real world, this never usually occurs.

## Performance versus Cost
* In software engineering, **performance** is "where the system meets performance goals specified by the customer"
* In the context of interaction with the world it is "where the system waits for the world, not the other way around"
* Where that interaction is with a human (in which "perceived waiting for the system is minimised") — i.e. it's an illusion

### Average-Case, Worst-Case and the n-th % Case

* In many safety-critical systems, worst-case performance is key — e.g. "The ESC will detect a skid condition within 30ms" (may even have to prove this)
* Others, average-case can be important — i.e. where algorithmic complexity is a factor based on average input
* Still others, n-th % case can also matter — e.g. 99% of all GET requests need to work

### Cost

Can include (but not limited to):

* Time and space constraints
* Hardware (CPU / GPU / RAM /Storage infrastructure)
* Network (Infrastructure / Service)
* Energy (Battery Life / Operating)
* Development ("Hardware is cheap but programmers are expensive")
* Fast code may be harder to write, harder to debug, more bugs deployed, less maintainable or even less portable

One of the best ways to facilitate decision-making in terms of weighing in cost versus performance is by graphing it and comparing where each option stands compared to the others.

### Performance

Technology advances, and it does improve performance. Some technologies have been developed solely to increase software efficiency, such as parallel computation, distributed computation, solid-state mass storage, and further increases in CPU and networking speeds.

#### Latency versus Bandwidth (freeway analogy)
* **Latency** — travel time along a freeway
* **Bandwidth** — width of a freeway
* Low latency plus high bandwidth means faster data
* As a rule of thumb: design for latency, buy bandwidth

#### Amdahl's Law
* Let S = number of distributed processors
* Let P = original program runtime
* Then the maximum speed up time <= 1/([1-P]+[P/S])



# Tradeoffs
Programmers are expected to write fast and efficient software at a low cost— but in the real world, this never usually occurs.

## Performance versus Cost
* In software engineering, **performance** is "where the system meets performance goals specified by the customer"
* In the context of interaction with the world it is "where the system waits for the world, not the other way around"
* Where that interaction is with a human (in which "perceived waiting for the system is minimised") — i.e. it's an illusion

### Average-Case, Worst-Case and the n-th % Case

* In many safety-critical systems, worst-case performance is key — e.g. "The ESC will detect a skid condition within 30ms" (may even have to prove this)
* Others, average-case can be important — i.e. where algorithmic complexity is a factor based on average input
* Still others, n-th % case can also matter — e.g. 99% of all GET requests need to work

### Cost

Can include (but not limited to):

* Time and space constraints
* Hardware (CPU / GPU / RAM /Storage infrastructure)
* Network (Infrastructure / Service)
* Energy (Battery Life / Operating)
* Development ("Hardware is cheap but programmers are expensive")
* Fast code may be harder to write, harder to debug, more bugs deployed, less maintainable or even less portable

One of the best ways to facilitate decision-making in terms of weighing in cost versus performance is by graphing it and comparing where each option stands compared to the others.

### Performance

Technology advances, and it does improve performance. Some technologies have been developed solely to increase software efficiency, such as parallel computation, distributed computation, solid-state mass storage, and further increases in CPU and networking speeds.

#### Latency versus Bandwidth (freeway analogy)
* **Latency** — travel time along a freeway
* **Bandwidth** — width of a freeway
* Low latency plus high bandwidth means faster data
* As a rule of thumb: design for latency, buy bandwidth

#### Amdahl's Law
* Let S = number of distributed processors
* Let P = original program runtime
* Then the maximum speed up time <= 1/([1-P]+[P/S])
