# Trees

![](https://miro.medium.com/max/975/1*PWJiwTxRdQy8A_Y0hAv5Eg.png)

## Common Terminology

- Node: component which may contain it’s own values, and references to other nodes
- Root: node at the beginning of the tree
- K: number that specifies the maximum number of children any node may have in a k-ary tree (in a binary tree, k = 2)
- Left: reference to one child node, in a binary tree
- Right: reference to the other child node, in a binary tree
- Edge: link between a parent and child node
- Leaf: node that does not have any children
- Height: number of edges from the root to the furthest leaf

## Traversals

- Allows to search for a node, print out the contents of a tree, and more
- Two categories of traversals of trees:
  - Depth first: prioritize going through the depth (height) of the tree first
    - Three methods for depth first: pre-order (root >> left >> right), in-order (left >> root >> right), and post-order (left >> right >> root)
  - Breadth first: iterates through the tree by going through each level of the tree node-by-node


## Binary Tree Vs K-ary Trees

- Trees can have any number of children per node, but Binary Trees restrict the number of children to two
- If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree
- K refers to the maximum number of children that each Node is able to have

## Big O

The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree. For example, in the above tree, w is 4.


## Binary Search Trees

A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

## Searching a BST

Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

## Big O for Binary Search

The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.

The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.

