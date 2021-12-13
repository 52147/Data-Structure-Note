# Data-Structure-Note

## Midterm Review

1. 

## Final Note

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
        
2. recursively tree

### Binary Tree
*  one node that only can have two children, which neamed them left and right
*  BT can be empty or consist a root, a left, a right.(left, right can be empty)


* uses:  
  * １.expression tree:　
    * The leaves are operands and nodes contain operator. 
    * apply in complier design
  * ２. Huffman coding tree:
    * used in data compression algorithm
    * Each alphabet is stored at a leaf
  * 3. Binary Search Tree: 
    * allows logarithmic time insertions and accessing of items, and priority queues.  



