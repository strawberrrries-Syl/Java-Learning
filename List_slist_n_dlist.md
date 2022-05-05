# Lists
Store a list of `int`s as an array.
**Disadwantages**:
* Insert ite, of beginning or middle. -> need time proportional to length of array.
* Arrays have. fixed length.

# Linked Lists
a recursive data type.
Made up of "nodes".

Each node has:
* an item;
* a reference to next node in list;
```java
public class ListNode {
  int item;
  ListNode next;
  
  public ListNode(int item, ListNode next) {
    this.item= item;
    this.next = next;
  }
  
  public ListNode(int item) {
    this(item, null);
  }
  
  // insert a item after this node.
  public InsertAfter(int item){
    this.next = new ListNode (item , next);
  }
}
// declare three nodes.
ListNode l1 = new ListNode(), l2 = new ListNode(), l3 = new ListNode();
l1.item = 7;
l2.item = 0;
l3.item = 6;

l1.next = l2;
l2.next = l3;
l3.next = null;
// l1->l2->l3

```

**Advantages:**
* inserting item int middle of linked list takes constant time if you have reference to previous node.
* moreover, list can keep growing until memory runs out.
**Disadvantages:**
* FInding the nth item of a likned list takes time proportional to n -> length of list.

# List of Objects
Reference any object by declaring a ref of type Object.
```java
public class SListNnode {
  public Object item;
  public SListNode next;
}

public class SList {
  private SListNode head;
  rivate int size;
  
  public SList() {
    head = null;
    size = 0;
  }
}
```
A List Class
2 problems with only using SListNodes.
1. Hard to insert from top
2. How do you represent on empty List
  You CANNOT just point the x -> null.
  *Solution* separate SList class maintains head of list. --> using SList.
  
# Private
A private mehod or field is invisible and inaccessible to other classes.
  
WHY want to use that? Teamworking.
1. Prevent data corrupted by other classes
2. You can improve the implementation without causing other classes to fail.
  
  
# Interface of a class
Prototypes for public methods, plus descriptions of their behaviors.
  
# Abstract Data Type (ADT):
A class with a well-defined interface, but implementation datails are hidden from other classes.
 
# Invariant
A fact about a data structure that is always true.
"A Data object always represents a valid date. "
 
Not all classes are ADTs! Some classes just store data (no invariants). 
 
## e.g. The SList ADT

Another advantage of SList class:

SList ADT enforces 2 invariants.
1. "size" is always correct.
2. list is never circularly linked.

Both goals accomplished because only SList methods can change the lists.

SList ensures this:
1. The fields of SList (head and size) are `private`.
2. No method of SList returns on SListNode.

# Double-linked Lists
Insert/deleting at frot of list is easy.
Insert/delete at end of list is hard for Single List.

```java
public class DListNode {
  Object item;
  DListNode next;
  DListNode prev;
}

public class DList {
  private DListNode head;
  private DListNode tail;
  
  Remove the tail node () {
    tail.prev.next = null;
    tail = tail.prev;
  }
}
```
## Sentinel //哨兵结点
A special node thatdoes not represent an item.
DList v.2: circularly linked.

Seninel is both the first and the last DListNode in a list. It should be totally implicite for user.
Then the DList's head will point to the sentinel. Size will be the nodes inside the link list except for the sentinel one.

DList invarians with sentinel:
1. For any DList d, d.head != null.
2. For any DListNode x, x.next != null;
3. For any DListNode x, x.prev!= nnull;
4. if x.next == y, then x == y.prev;
5. if x.prev == y, then x == y.next;
6. A DList's `size` variable is # of DListNodes, NOT COUNTING sentinel.
7. Empty DList: sentinel's prev & next field point to itself.

