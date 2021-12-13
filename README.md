# Data-Structure-Note

## Midterm Review

1. 

## Final Note

### Recursion
* using stack
* 

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
        
2. recursively tree: a tree is either empty or consists of a root and
zero or more subtrees. 

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


* A data structure that supports insertion, searching, and deletion in O(log N) average time. 
* one node that can only have two children, which neamed them left and right
* BT can be empty or consist a root, a left, a right.(left, right can be empty)
* all smaller keyed nodes are in the left subtree and all larger keyed nodes are in the right subtree. 
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
* The running time for most operations is O(log N) on average. 
* the worst-case time is O(N) per operation.



