# Rooted Trees
`Tree`: Set of nodes & edges that connect them.
* Exactly one path between any 2 nodes.

`Path`: Connected sequence of edges.

`Rooted Tree`: One distinguished node is called the root.

Every node c, except root, has one parent p, the first node on path from c to the root. c is p's child. Root has no parent. A node can have any number of children. 

* Leaf: Node with no children.
* Siblings: Nodes with same parent.
* Ancestors of a node d: nodes on path from d to root. Including d, d's parent, d's grandparent ...  root.
* If a is an ancestor of d, then d is descendant of a.
* Length of path: Number of edges in path.
* Depth of node n: length of path from n to root. Depth of root is zero.
* Height of node n: length of path from n to its deepest descendant. Height of leaf node is zero.  高度，距离叶子结点的path。Height of a tree = height of the root.
* Subtree rooted at n: tree formed by n & its descendants.
* A binary tree: No node has > 2 children, every child is a left child or a right child, even if it's the only child.

# Representing Rooted Trees
* Each hash 3 references: item, parent, children stroed in a list.
* Another option: shiblikngs are directly linked. 
```java
class SibTreeNode{
    Object item;
    SibTreeNode parent;
    SibTreeNode firstChild;
    SibTreeNode nextSibling;
}

Public class SibTree{
    SibTreeNode root;
    int size;
}

```

 # Tree traversal.
`Traversal` : amnner of visiting each nodeopn a tree once`
## Preorder traversal
* preorder traversal: visit each node begore recursively visiting its children, left to right.Root visited first.
* Each node has been visited once, so a preorder traversal takes O(n) time, where n is number of nodes in tree. self-left-right // self-sib-child

## Postorder Traversal: 
Visit each node's children(left-right) before the node itself. left-right-self // child-self-sib

## Inorder Traversal:
Binary trees: left-self-right

## Level-order traversal:
Visit root, then all depth-1 nodes(left to right), then all depth-2 nodes, etc. `Not recursive`.

Use a queue, which initially contains only the root. Repeat (BFS, 辅助队列)


