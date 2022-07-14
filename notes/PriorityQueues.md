# Definition:
Entries consist of key and value.
The total order is defined on the keys. 
（堆）

Operations: 
* Identify or remove entry whose key is lowest. (But no other entry).
* Any key mabe inserted at any time.

# Commonly used
As "event queues" in simulations. Key is the time event takes place. Value is description of event.

# Binary heap:
An implementation of priority queues.
## Definitaion: （完全二叉树-除了最后一行，全部枝都有值）
* A cpmplete binary tree. -- > Every row(level) of the tree is full, except bottom row.
* Entries satisfy the heap-order property:
no child has a key less than its parent's key.
* Often stored as arryas of entries by level-order traversal.
* Mapping of nodes to indices: level numbering.
    * Node i's children are 2i & 2i+1;
    * Parent is i/2.
* Each tree node has 2 references(key, value), or references an "Entry" object. 
1. 是完全二叉树
2. 根节点小于两个字节点

# Operations
1. Entry min(); --> root is the smallest one.
2. insert(Object k, object v)
    * let x be new entry (k, v).
    * place x in bottom level of tree, at first free spot from left. i.e. first free location in array
    * Entry bubbles up tree until heap-order property is satisfied.
         Repeat
        * compare x's key with its parent's key. 
        * If x's key is less, exchange.
3. removeMin();
    用最后一个值代替空缺，如果x比两个字节点的一个小，swap x with it‘s minimum child。repeat。

# Every subtree of a binary heap is a binary heap.


