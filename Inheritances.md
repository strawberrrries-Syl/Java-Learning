# Inheritance. (Polymorphism)
```java
public class TailList extends SList{
  /* head and size inherited from SList. */
  private SListNode tail;
}
```
TailList is a `subclass` of SList.

SList is the `superclass` of TailLists.

A subclass can modify a superclass in 3 ways.
1. It can declare new fields.
2. It can declare new Methods.
3. It can override old methods with new implementations.
4. It can keep old things.

# inheritance & Constructors
Java executes a TailList constructor, but first it executes SList() constructor.
```java
public TailList() {
  // SList() sets size = 0; head = null     <-- zero parameter constructor called by default
  tail = null;
}

// to change:
public TailList(int x) {
  super(x);     // must be first statement in constructor
  // or this();
  tail = null;
}
```

# Invoking overriden methods
```java
public void inserFront(Object obj) {
  super.insertFront(obj);   // <-- You don't need to make sure this line is the first line of the method
  if(size == 1) {
    tail = head;
  }
}
```

`Protected` field/method is visible to declaring class & all its subclasses.
`Private` fields aren't visible to subclasses.

# Dynamic method lookup
Every TailList is an SList.
```java
SList s = new TailList(); // fine
TailList t = new SList(); // Compiletime-error
```
Static type: the type of a variable     -->  SList
Dynamic type: the class of the object the variable references.        --> TailList

When we invoke overridden method, Java calls method for the object `dynamic type`, regardless of `static type`. ->Dynamic method look up

# IS_A and HAS_A test
* xxa is a xxb --> xxa extand to xxb
* xxb has a xxa --> xxa is a field of xxb

**Important:** 
1. Inheritance lets you guarantee that all classes gourped under a certain supertype have all the methods that the supertype has.
2. Final class cannot be overrided.
3. Overriden is not the same as Overloaded
