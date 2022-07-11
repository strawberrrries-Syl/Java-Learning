# Binary search trees

## Ordered dictionary:
Dictionary in which keys are ordered, like in a heap.

Insert, find, remove entries.
Quickly find entry with minimum or maximum key, or entry nearist another entry.

根节点左边的都比根小，根右边的都比根大。
## Binary search tree invariant:
For any node X, evert key in left subtree of X is <= rX'key, inright is >= X'key.

Inorder traversal of binary saerch tree. Visit nodes in sorted order.
二叉搜索树，中序遍历可以按小-大顺序便利。

## Operations
### 1. Entry find(Object k);
### 2. How to find smallest key >= k; or largest key <= k:?

When searching down tree for a key k that is not in tree, we encounter both :
* node containing smallest key > k
* node containing largest key < k.


### 3. delete 
```Entry remove(Object k);```

Find a node n with key k;

Return null if k not in tree;

* If n has no children, detach if from parent.
* If n has one child, move n's child up to take n's place.
* If n has two children. Let X be node in n's right subtree with the smallest key.