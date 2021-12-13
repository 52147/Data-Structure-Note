# Data-Structure-Note

## Midterm Review

1. 

## Final Note

### Doubly Linked List

### Recursion
* A recursive method is a method that either directly or indirectly makes a call to itself.
* A recursive method is defined in terms of a smaller instance of itself. 
 * Proofs by induction:
 * 1. a statement is true for a smallest case 
 * 2. and can show that one case implies the next case
 *   => then we know the statement is true for all cases.
 * Base case(to stop):
 * Any recursive call must make progress toward a base case(can be computed without recursion) in order to terminate eventually.

* Fibonacci numbers: A sequence of numbers in which the ith number is the sum of the two previous numbers.

* using stack:
 * Java implements recursive methods by using an internal stack of activation records.
 * The stack of activation records is used because methods return in reverse order of their invocation
 * Recursion can always be removed by using a stack to save space.

* Recursion can be proved by induction.


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
* 1. preorder : vist root node-> left subtree of the root -> right subtree of the root
* 2. postorder : vist left subtree of the root -> right subtree of the root -> root node
* 3. inorder : vist left subtree of the root -> root node -> right subtree of the root 
* Time Complexity: 
 * linear
 * each node is output only once, takes constant time per node.
 * O(N)
* 

### Binary Tree


* supports insertion, searching, and deletion in O(log N) average time. 
* one node that can only have two children, which neamed them left and right
* BT can be empty or consist a root, a left, a right.(left, right can be empty)
* smaller keyed nodes are in the left subtree and larger keyed nodes are in the right subtree. 
* Duplicates are not allowed.



* uses:  
  * １.expression tree:　
    * The leaves are operands and nodes contain operator. 
    * apply in complier design
  * ２. Huffman coding tree:
    * used in data compression algorithm
    * Each alphabet is stored at a leaf
  * 3. Binary Search Tree: 
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
