# Stack and the Heap --> Where things live
The heap stores all objects, including arrays, and all class variables.

The stack strores all local variables and methods, including parameters.
```
methods()  |   Objects
           |
stack      |   Heap
```
*Instance Variables:* in heap. declared inside a `class` but not inside a method.

*Local Variables:* in stack. declared inside a `method`, including method parameters. Temporary and live only as long as the method is on the stack.

* When a method is called, Java creates a stack frame (aka activation record) stores the parameters & local variables.

**Difference between heap and stack**
1. variables in stack only needs to be claimed. After that, you can use them. System will handle the trash. But things in heap need to be free manually after using(Java will handle your trash!)
2. Stack is quicker than heap (reading or writing). But stack only can store things unchangable.
3. For primitive types, all in stack. For wraped types `like Integer, String, Double`, all in heap.
4. Normally, new() constructor always put data in heap.

 When method finishes, its stack frame is erased (garbage collected).

`Method: Thread.dumpstack();` A method to print out the methods' order. Good for debugging. (in java.lang lib)

## Parameter Passing
All parameters are passed bu value --> **COPIED**. Method cannot change the original one.

But when a parameter is a reference. The reference is copied but not the things at points to.

* Objects used constructors to generate always is reference. 


# Binary Search

## Aim: 
Search a sorted array. for value "FindMe". return index or FAILURE.

## How:
### Recursion base cases:
1. findMe = middle element: return its index.
2. Subrray of length zero: return FAILURE.
 *When changing middle, remember to add 1.

How fast? n...n/2...n/4...n/8..1?

Takes log2n recrsive bsearch calls.

There are enough stack space for a few thousands of stack frames **ONLY**.

# Scope & recursion (Shadowed?)

Scope of a variable: portion of program that can access the variable.
1. Class variables: in scope everywhere in the class, except when 


# Life and Death of an Object
**The Garbage Cpllector(gc)**

