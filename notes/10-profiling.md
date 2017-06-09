[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Performance Profiling
> It is almost impossible to identify performance bottlenecks before the program is completely working. Programmers almost never target the right area ahead of time.

— McConnell

## Tools for Performance Testing
Mainly divided into two parts:

* Generating load on the system
* Measuring performance under load

### Manual Instrumentation
* Involves diagnostics within code
* Is easy to implement and works in almost every environment
* However involves modifying existing codebase for print statements and then having to remove these print statements once finished

### Code Profiling
* External tools that analyse code at the function or even line-level
* Measures performance by timing code execution given heavy load / input

### Load Testing
* Also known as stress-testing software
* Not just restricted to code performance, but how the software performs in the real world (i.e. simulating network requests, etc.)

#### Profiling Case Study: Merge Sort
Suppose have the merge sort algorithm implemented in Python:

* A code profiler would determine that the `merge(list1, list2)` operation within the `mergeSort(list)` method is causing the performance bottleneck
* A line-profiler would determine that the recursive calls and the array slicing within `merge()`  takes the longest to execute
* Because of this, the result of our profiling tests indicate we must avoid recursive calls to boost performance
* As a result, our merge sort algorithm would need to be re-written to use an iterative approach