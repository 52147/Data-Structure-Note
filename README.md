# Data-Structure-Note

## Midterm Review

1. 

## Final Note

### Priority Queues
* a priority queues is an abstract data type similar to a regular queus or stack data structure
* in whuch each element additionaly has a "priority" associated with it.
* In priority queues, an element with high priority is serverd before an element with low priority.
* Misconception:
   *  A priotity queues is not the same as heap.
   *  A heap is a data structure, a priority is a abstract data type.
   *  A heap is a wat to implement a priority queue.
* Implementation:
   * use array or linked list
   * use heap
* Time complexity
   * use array or linked list
      * insertion and deletion -> O(1)
      * other operation -> O(N)  
   * use heap
       * insertion and deletion -> O(logN) 
### Heap
* A heap is a special type of Binary tree.
* heap propertiesL
   * is a complete binary tree.
   * the value of each node must be no greater thatn(or no less than) the value of its child node.
* Time complexity:
   * insertion of an element into the heap need O(logN) time
   * deletion of an element  from the heap need O(logN) time
   * the maximum/ minimum value in the heap can be obtained with O(i) time. 

* 2 kinds of Heap:
   * 1. Max heap
       * each node in the heap has a value no less than its child nodes.
       * thus, the top element(root node) has the largest value in the heap. 
   * 2. Min heap 
       * each node in the heap has a value no loger than its child nodes.
       * thus, the top element(root node) has the smallest value in the heap 

![image](https://user-images.githubusercontent.com/79159894/145886189-3f9037e7-5f5e-43d9-80f7-94e2721a115b.png)


* Is the following tree a heap? 
* NO
* although all node have smaller value than their child nodes, it is not a complete binary tree.

![image](https://user-images.githubusercontent.com/79159894/145888282-157c666e-1ded-4422-b100-6cea59a83ccd.png)


### Doubly Linked List
* A doubly linked list allows bidirectional traversal by storing two links per node.
* Symmetry demands that we use both a head and a tail and that we support roughly twice as many operations.
* When we advance past the end of the list, we now hit the tail node instead of null.
   * An empty doubly linked list: 
```
head.next == tail or tail.prev == head
```
* Insertion and removal involve twice as many link changes as for a singly linked list.
  - to remove x we have to change a’s next link and b’s prev link.
```
newNode = new DoublyLinkedListNode( x );
newNode.prev = current; // Set x's prev link
newNode.next = current.next; // Set x's next link
newNode.prev.next = newNode; // Set a's next link
newNode.next.prev = newNode; // Set b's prev link
current = newNode;
```
* The remove operation can proceed from the current node because we can obtain the previous node instantly.
```
current.prev.next = current.next; // Set a's next link
current.next.prev = current.prev; // Set b's prev link
current = head; // So current is not stale
```



### Recursion
* A recursive method is a method that either directly or indirectly makes a call to itself.
* A recursive method is defined in terms of a smaller instance of itself. 
   - Proofs by induction:
   * 1. a statement is true for a smallest case 
   * 2. and can show that one case implies the next case
   *  => then we know the statement is true for all cases.
 * Base case(to stop):
   * Any recursive call must make progress toward a base case(can be computed without recursion) in order to terminate eventually.

* Fibonacci numbers: A sequence of numbers in which the ith number is the sum of the two previous numbers.

* Using stack to implement:
  * Java implements recursive methods by using an internal stack of activation records.
  * because methods return in reverse order of their invocation
  * Recursion can always be removed by using a stack to save space.

* Activation record:
  *  is used to manage the information needed by a single execution of a procedure. 
  *  is pushed into the stack when a procedure is called and it is popped when the control returns to the caller function.




### Tree
1. nonrecursively tree
   * consistd of a set of nodes and a set of directed edges
   * application: 
     * File system : 
       * use root and childre to reach hierarchical file system, it allows user to organize their data logically.
       * ex: Unix, VAX/VMS, and windows/DOS
     * Unix fily system:
       * the root of directory is mark, mark has 3 children books, course, login
   * rooted tree's properties:
   
     * 1. One root node(has no parent); depth: 0;
     * 2. Every node is connected by an edge from one other node. 
          * ex: node c is connected with node p. -> Node p is c' s parent, and c is one of p's children.
          * A tree with N node has N-1 edges.
     * 3. path length: the number of edges from the root to each node. 
     * 4. leaf: node that has no children is called an leaf
     * 5. depth: length of the path from the root to the node. the depth of root is 0. the depth of any node is one more that its parent.
     * 6. height: length of the path from the node to the deepest leaf.
     * 7. size: The number of descendants a node has (including the node itself).
        
2. recursively tree: a tree is either empty or consists of a root and zero or more subtrees. 

### Tree traversal
* traversal: count how many descendants the node has.
* can be implemented recursive or non recursive

![image](https://user-images.githubusercontent.com/79159894/145777204-c8cb32d0-4272-4652-8a70-39950d54660b.png)

1. preorder : vist root node-> left subtree of the root -> right subtree of the root
   *  A, B, D, C, E, G, F, H, I
3. postorder : vist left subtree of the root -> right subtree of the root -> root node
   * D, B, G, E, H, I, F, C, A
4. inorder : vist left subtree of the root -> root node -> right subtree of the root
   * B, D, A, G, E, C, H, F, I

* Time Complexity: 
  * linear
  * each node is output only once, takes constant time per node.
  * O(N)


### Binary Tree


* supports insertion, searching, and deletion in O(log N) average time. 
* one node that can only have two children, named them left and right
* BT can be empty or consist a root, a left, a right.(left, right can be empty)
* smaller keyed nodes are in the left subtree and larger keyed nodes are in the right subtree. 
* Duplicates are not allowed.



* uses:  
 1. expression tree:　
    * The leaves are operands and nodes contain operator. 
    * apply in complier design
 2. Huffman coding tree:
    * used in data compression algorithm
    * Each alphabet is stored at a leaf
 3. Binary Search Tree: 
    * allows logarithmic time insertions and accessing of items, and priority queues.  

* Time Complexity: 
  * most operations is O(log N) on average. 
  * the worst-case time is O(N) per operation.


### Hash Table
* A table used to implement a dictionary(a set) in constant time per operation.
* Hashing: The implementation of hash tables is called hashing, and it performs insertions, deletions, and finds in constant average time.

* Use index to store the item:
  * one-to-one(one item in one index)
    * converts the item into an integer suitable to index an array where the item is stored. If the hash function were one to one, we could access the item by its array index.
  * Not one-to-one -> collision: several items collide at the same index and cause a collision.
    * collision : The result when two or more items in a hash table hash out to the same position. This problem is unavoidable because there are more items than positions.
* BST vs. Hash Table:
  * if you do not need order statistics and are worried about nonrandom inputs, use hash table instead of BST
* Time Complexity: 
  *  is based on statistical properties rather than the random-looking input(BST). 



### Graph
* graph is a non-linear data structure consisting of vertices an edges.
* graph has the closet resemblance to our daily life.
* ex: the friendship circle is a hugh undirected graph
* Figure 1:
![image](https://user-images.githubusercontent.com/79159894/145889087-dfdd5b7a-6fc1-4989-add0-9fc989f51e83.png)


* 3 Types of graph
* 1. undirected graphs
     * the edges between any 2 vertices do not have a direction, indicating a 2-way relationship.
* 2. directed graphs
     * the edges between any 2 vertices  are directional.
![image](https://user-images.githubusercontent.com/79159894/145889637-0c2b49a9-bed7-47f6-bb46-3e0170bc71e7.png)

* 3. weighted graphs
     * each edge has an associtated weight.
     *  the weight can be of any metric, such as time, distance, size, etc.
     *  ex: city map
   ![image](https://user-images.githubusercontent.com/79159894/145889929-8defb5e0-0d56-473f-b147-3ec8d0c51c81.png)
     *   In this figure, each edge is marked with the distance, which can be regarded as the wight of that edge.

* Terminologies:
 * Vertex: nodes
 * Edge: tha connection between 2 vertices
 * Path: the sequence of vertices to go through from one vertex to another.
   * ex: In figure 1, a path from A to C is [A,B,C], or [A, G, B, C], or [A, E, F, D, B, C].
   * Note: there can be multiple paths between 2 vertices.
 * Path length: the number of edges in a path.
   * In figure 1, the path lengths from person A to C are 2, 3, and 5, respectively.
 * Cycle: a path where the starting point and endpoint are the same vertex.   
   * In figure 1, [A, B, D, F, E] forms a cycle.
   * Similarly, [A, G, B] forms another cycle.
 * Negative weight cycle:
   * In a "weighted graph", if the sum of the weights of all edges of a cycle is a negative value, it is a negative weight cycle.
   * In this figure, the sum of weight is -3.
![image](https://user-images.githubusercontent.com/79159894/145893999-e934bf8d-a4e9-49f7-83d2-9df39e58fe2e.png)

 * Connectivity: if there exists at least one path between 2 vertices, these 2 vertices are connected.  
   * In figure 1, A and C are connected because there at least 1 path connecting them.
 * Degree of a vertex: 
   * the term "degree" applies to unweighted graphs.
   * the degree of a vertex is the number of edges connecting the vertex.
   * In figure 1, the degree of vertex A is 3 becaause 3 edges are connecting it.
 * In-degree: 
   * is a concept in directed graphs.
   * If the in-degree of a vertex is d, there are d directional edges incident to the vertex.
   * In figure 2, A's indegree is 1, the edge from F to A.
 * Out-degree:
   * is a concept in directed graphs.
   * if the out-degree of a vertex ia d, there are d edges incident from the vertex.
   * In figure 2, A's outdegree is 3, the edges A to B, A to C, and A to G.     

### Disjoint Set

