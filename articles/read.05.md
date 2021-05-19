# Linked List

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2013/03/Linkedlist.png)

* Linked list: data structure that contains nodes that links/points to the next node in the list.

* Most defining feature of a linked list is that each Node references the next Node in the link.

* Node: individual items/links that live in a linked list, each node contains data for each link.

* Next: each node contains property called next, property contains the reference to the next node.

* Head: reference type of type Node to the first node in a linked list.

* Current: reference type of type Node that is currently being looked at.

* Big O notation: way of evaluating the performance of an algorithm.

* There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.

* Linked lists Big O equations O(1) and O(n)

* An O(1) function takes constant time.

* An O(n) function is linear.

* A linked list is usually efficient when it comes to adding and removing most elements, but it can be very slow to search and find a single element.


## Types of linked list

* Singly Linked List : 

It is the most common. Each node has data and a pointer to the next node.

* Doubly Linked List :

We add a pointer to the previous node in a doubly-linked list. Thus, we can go in either direction: forward or backward.

* Circular Linked List : 

A circular linked list is a variation of a linked list in which the last element is linked to the first element.


## Parts of a linked list

A linked list can be small or huge, but no matter the size, the parts that make it up are actually fairly simple. A linked list is made up of a series of nodes, which are the elements of the list.

## Growing a linked list

like with an array, we can add elements and remove elements from a linked list. But unlike arrays, we don’t need to allocate memory in advance or copy and re-create our linked list, since we won’t “run out of space” the way we might with a pre-allocated array.

