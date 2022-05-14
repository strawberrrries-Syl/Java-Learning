# `instanceof`
instanceof can check the static type of an object. Same object type -> true.

# `Abstract` Classes
A class whose sole purpose is to be extended.

```java
public abstract class List {
  protected int size;
  public int length() {
    return size;
  }
  
  public abstract void insertFront(Object item);    // tell subclass that they must have this method
}


List myList;
myList = new List();    // COMPILE_TIME_ERROR  no List object exists

```
Abstract class lack of impletation

## An example of a feasible subclass of List
```java
public class SList extends List {
  // inherits 'size'
  protected SListNode head;
  // inherits 'length()'
  public void insertFront(Onject item) {
    head = new SListNode(item, head);
    size++;
  }
}
```
* An non-abstract class may never contain an abstract method
* inherit one without providing an implementation.
```java
List myList = new SList();
myList.insertFront(obj);      // now these work
```

## !
One list sorter can sort every kind of List
```java
public void listSort(List l) {...}

```
You can use this method on:

* SubClasses of List: SList, DList, TailList, 
* TimedList: records time spent doing operations.
* TransactionList: logs all changes on a disk for power outrage.



# Java Interfaces
`interfaces` = public method prototype & behaviors;

`Java interfaces` = "interface" keyword

Java interface is like abstract class; 2 differences.
1. A class can inherit from only one class, but can "implement" (inherit from) as many Java interfaces as you like.
2. A Java interface cannot:
* implement any methods,
* include any fields except "static final" constants. Only contains method prototypes & constants.
