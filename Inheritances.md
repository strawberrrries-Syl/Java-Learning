# Inheritance
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
SList s = new TailList(); // fine
TailList t = new SList(); // Compiletime-error

Static type: the type of a variable     -->  SList
Dynamic type: the class of the object the variable references.        --> TailList

