---
title: "More reasoning about binary search trees"
published: true
morea_id: experience-binary-search-trees-2
morea_type: experience
morea_summary: "Apply your learning about binary trees some more."
morea_sort_order: 2
morea_labels:
 - Homework
---

### Binary Search Trees

**4.** (4 pts) Suppose you have some data keys sorted in an array and you want to construct a _**balanced binary search tree**_ from them. Assume a tree node representation `TreeNode` that includes instance variables `key`, `left`, and `right`.

**a.**  Write pseudocode (or Java if you wish) for an algorithm that constructs the tree and returns the root node. (We won't worry about making the enclosing `BinaryTree` class instance.) You will need to use methods for making a new `TreeNode`, and for setting its left and right children.

_Hints: First, identify the array location of the key that would have to be
the root of the balanced BST. Now think about how BinarySearch works on the
array. Which item does it access first in any given subarray it is called
with? Using a similar strategy a simple recursive algorithm is possible._

**b.**   What is the Θ cost to construct the tree? How does the expected runtime of BinarySearch on the array compare to the expected runtime of search in the tree you just constructed? 



**5.** (3 pts) In `Tree-Delete` (page 298 or as shown in the web notes), when node _z_ has two children, we arbitrarily decide to replace it with its successor. We could just as well replace it with its predecessor. 

**a.**   Rewrite `Tree-Delete` to use the predecessor rather than the successor. Modify this code just as you need to.
    
    
      TREE-DELETE(T, z)
      1  if z.left == NIL
      2      TRANSPLANT(T, z, z.right)
      3  elseif z.right == NIL
      4     TRANSPLANT(T, z, z.left)
      5  else y = TREE-MINIMUM(z.right)  // successor
      6      if y.p != z
      7          TRANSPLANT(T, y, y.right) 
      8          y.right = z.right
      9          y.right.p = y
      10      TRANSPLANT(T, z, y)
      11      y.left = z.left
      12      y.left.p = y
    

**b.**   Some computer scientists have argued that if equal priority were given to replacing the successor and the predecessor to not skew deletions on one side, better performance might result. How might `Tree-Delete` be modified to implement such a strategy? (_Hint:_ think about last week's topics.)
