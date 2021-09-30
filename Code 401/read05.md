# Linked List

## Big O: Analysis of Algorithm Efficiency

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

* Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

* Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.


## What is a Linked List?

A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

There are two types of Linked List:

* Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
* Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

* A circular linked list is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list.

## What’s a Linked List, Anyway ? 

One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

- **To insert an element into a linked list:**

* First, we find the head node of the linked list.
* Next, we’ll make our new node, and set its pointer to the current first node of the list.
* Lastly, we rearrange our head node’s pointer to point at our new node.

- **To insert an element at the end of a linked list:**

* Find the node we want to change the pointer of (in this case, the last node)
* Create the new node we want to insert and set its pointer (in this case, to null)
* Direct the preceding node’s pointer to our new node.

## LinkedList vs Arrays

<img src="https://cdn.spotle.ai/7262/large/Z6jGwVJMAU.PNG">





