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
